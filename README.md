# Instruções

### ID
* No campo ID não deixei como AUTOINCREMENT, pois criei um espaçamento entre cada país caso haja a necessidade de alocar algum novo cadastro e seja necessário manter em ordem alfabética.
* Outra observação associada a observação anterior é que comecei os registros pelo número 101 para manter o padrão de 3 caracteres. Podia ter começado com 001, mas quis evitar qualquer corte nos zeros em qualquer linguagem que fosse utilizar esses dados. Esta razão também justifica eu ter deixado o AUTOINCREMENT de fora.

### tx_name_pt
* Este formato sempre utilizo na criação dos meus campos para que eu identifique facilmente o formato de cada campo.
Exemplo:
* __ID__ e __CD__ para códigos;
* __TX__ para string;
* __VL__ para números e float;
* __CK__ para check.

* O __pt__ no final coloquei como referência ao Português, pois pretendo adicionar tx_name_en (Inglês) ou em outro idioma para utilizar em sistemas com multilinguagens.


## Criar a table
```
CREATE TABLE IF NOT EXISTS paises (
  id tinyint(3) unsigned NOT NULL,
  tx_name_pt varchar(50) NOT NULL,
  tx_sigla varchar(2)
  PRIMARY KEY (id)
)
```
## Inserir os dados
```
INSERT INTO paises (id, tx_name_pt, tx_sigla) VALUES
(101, 'Afeganistão', 'AF'),
(104, 'Africa do Sul', 'ZA'),
(107, 'Albânia', 'AL'),
(110, 'Alemanha', 'DE'),
(113, 'Andorra', 'AD'),
(116, 'Angola', 'AO'),
(119, 'Anguilla', 'AI'),
(122, 'Antartica', 'AQ'),
(125, 'Antígua e Barbuda', 'AG'),
(128, 'Antilhas Holandesas', 'AN'),
(131, 'Arábia Saudita', 'SA'),
(134, 'Argélia', 'DZ'),
(137, 'Argentina', 'AR'),
(140, 'Armênia', 'AM'),
(143, 'Aruba', 'AW'),
(146, 'Austrália', 'AU'),
(149, 'Áustria', 'AT'),
(152, 'Azerbaidjão', 'AZ'),
(155, 'Bahamas', 'BS'),
(158, 'Bangladesh', 'BD'),
(161, 'Barbados', 'BB'),
(164, 'Bareine', 'BH'),
(167, 'Belarus', 'BY'),
(170, 'Bélgica', 'BE'),
(173, 'Belize', 'BZ'),
(176, 'Benelux', 'BX'),
(179, 'Benin', 'BJ'),
(182, 'Bermudas', 'BM'),
(185, 'Bolívia', 'BO'),
(188, 'Bósnia e Herzegóvina', 'BA'),
(191, 'Botswana', 'BW'),
(194, 'Brasil', 'BR'),
(197, 'Brunei Darussalam', 'BN'),
(200, 'Bulgária', 'BG'),
(203, 'Burkina Faso', 'BF'),
(206, 'Burundi', 'BI'),
(209, 'Butão', 'BT'),
(212, 'Cabo Verde', 'CV'),
(215, 'Camarões', 'CM'),
(218, 'Camboja', 'KH'),
(221, 'Canadá', 'CA'),
(224, 'Catar', 'QA'),
(227, 'Cazaquistão', 'KZ'),
(230, 'Chade', 'TD'),
(233, 'Chile', 'CL'),
(236, 'China', 'CN'),
(239, 'Chipre', 'CY'),
(242, 'Colômbia', 'CO'),
(245, 'Comores', 'KM'),
(248, 'Congo', 'CG'),
(251, 'Costa do Marfim', 'CI'),
(254, 'Costa Rica', 'CR'),
(257, 'Croácia', 'HR'),
(260, 'Cuba', 'CU'),
(263, 'Dinamarca', 'DK'),
(266, 'Djibuti', 'DJ'),
(269, 'Dominica', 'DM'),
(272, 'Egito', 'EG'),
(275, 'El Salvador', 'SV'),
(278, 'Emirados Árabes Unidos', 'AE'),
(281, 'Equador', 'EC'),
(284, 'Eritréia', 'ER'),
(287, 'Escritório para Harmonização no Mercado Interno', 'EM'),
(290, 'Eslováquia', 'SK'),
(293, 'Eslovenia', 'SI'),
(296, 'Espanha', 'ES'),
(299, 'Estados Unidos da América', 'US'),
(302, 'Estônia', 'EE'),
(305, 'Etiópia', 'ET'),
(308, 'Federação Russa', 'RU'),
(311, 'Fiji', 'FJ'),
(314, 'Filipinas', 'PH'),
(317, 'Finlândia', 'FI'),
(320, 'França', 'FR'),
(323, 'Gabão', 'GA'),
(326, 'Gambia', 'GM'),
(329, 'Gana', 'GH'),
(332, 'Geórgia', 'GE'),
(335, 'Geórgia do Sul e Ilhas Sandwich do Sul', 'GS'),
(338, 'Gibraltar', 'GI'),
(341, 'Granada', 'GD'),
(344, 'Grécia', 'GR'),
(347, 'Groenlândia', 'GL'),
(350, 'Guadalupe', 'GP'),
(353, 'Guam', 'GU'),
(356, 'Guatemala', 'GT'),
(359, 'Guiana', 'GY'),
(362, 'Guine', 'GN'),
(365, 'Guiné Bissau', 'GW'),
(368, 'Guine Equatorial', 'GQ'),
(371, 'Haiti', 'HT'),
(374, 'Holanda', 'NL'),
(377, 'Honduras', 'HN'),
(380, 'Hong-Kong', 'HK'),
(383, 'Hungria', 'HU'),
(386, 'Iêmen', 'YE'),
(389, 'Ilha Bouvet', 'BV'),
(392, 'Ilha do Homem', 'IM'),
(395, 'Ilha Natal', 'CX'),
(398, 'Ilha Norfalk', 'NF'),
(401, 'Ilhas Cayman', 'KY'),
(404, 'Ilhas Cocos', 'CC'),
(407, 'Ilhas Cook', 'CK'),
(410, 'Ilhas do Canal', 'GG'),
(413, 'Ilhas Faroe', 'FO'),
(416, 'Ilhas Heard e McDonald', 'HM'),
(419, 'Ilhas Malvinas', 'FK'),
(422, 'Ilhas Marianas do Norte', 'MP'),
(425, 'Ilhas Marshall', 'MH'),
(428, 'Ilhas Menores', 'UM'),
(431, 'Ilhas Salomão', 'SB'),
(434, 'Ilhas Turks e Caicos', 'TC'),
(437, 'Ilhas Virgens (Britânicas)', 'VG'),
(440, 'Ilhas Virgens (U.S.)', 'VI'),
(443, 'Ilhas Wallis e Futura', 'WF'),
(446, 'India', 'IN'),
(449, 'Indonésia', 'ID'),
(452, 'Indonésia', 'ID'),
(455, 'Irã', 'IR'),
(458, 'Irã', 'IR'),
(461, 'Iraque', 'IQ'),
(464, 'Iraque', 'IQ'),
(467, 'Irlanda', 'IE'),
(470, 'Irlanda', 'IE'),
(473, 'Islândia', 'IS'),
(476, 'Islândia', 'IS'),
(479, 'Israel', 'IL'),
(482, 'Israel', 'IL'),
(485, 'Itália', 'IT'),
(488, 'Jamaica', 'JM'),
(491, 'Japão', 'JP'),
(494, 'Jersey', 'JE'),
(497, 'Jordânia', 'JO'),
(500, 'Kiribati', 'KI'),
(503, 'Kuwait', 'KW'),
(506, 'Laos', 'LA'),
(509, 'Lesoto', 'LS'),
(512, 'Letônia', 'LV'),
(515, 'Líbano', 'LB'),
(518, 'Libéria', 'LR'),
(521, 'Líbia', 'LY'),
(524, 'Liechtenstein', 'LI'),
(527, 'Lituânia', 'LT'),
(530, 'Luxemburgo', 'LU'),
(533, 'Macau', 'MO'),
(536, 'Madagascar', 'MG'),
(539, 'Malásia', 'MY'),
(542, 'Malawi', 'MW'),
(545, 'Maldivas', 'MV'),
(548, 'Mali', 'ML'),
(551, 'Malta', 'MT'),
(554, 'Marrocos', 'MA'),
(557, 'Martinica', 'MQ'),
(560, 'Maurício', 'MU'),
(563, 'Mauritânia', 'MR'),
(566, 'México', 'MX'),
(569, 'Mianmá', 'MM'),
(572, 'Micronésia', 'FM'),
(575, 'Moçambique', 'MZ'),
(578, 'Mônaco', 'MC'),
(581, 'Mongólia', 'MN'),
(584, 'Mont Serrat', 'MS'),
(587, 'Montenegro', 'ME'),
(590, 'Namíbia', 'NA'),
(593, 'Nauru', 'NR'),
(596, 'Nepal', 'NP'),
(599, 'Nicarágua', 'NI'),
(602, 'Níger', 'NE'),
(605, 'Nigéria', 'NG'),
(608, 'Noruega', 'NO'),
(611, 'Nova Caledônia', 'NC'),
(614, 'Nova Zelândia', 'NZ'),
(617, 'Omã', 'OM'),
(620, 'Palau', 'PW'),
(623, 'Panamá', 'PA'),
(626, 'Papua Nova Guiné', 'PG'),
(629, 'Paquistão', 'PK'),
(632, 'Paraguai', 'PY'),
(635, 'Peru', 'PE'),
(638, 'Pitcairn', 'PN'),
(641, 'Polinésia Francesa', 'PF'),
(644, 'Polônia', 'PL'),
(647, 'Porto Rico', 'PR'),
(650, 'Portugal', 'PT'),
(653, 'Quênia', 'KE'),
(656, 'Quirguistão', 'KG'),
(659, 'Reino Unido', 'GB'),
(662, 'República Centro Africana', 'CF'),
(665, 'República da Coréia', 'KR'),
(668, 'República da Macedonia', 'MK'),
(671, 'República da Moldova', 'MD'),
(674, 'República Dem. Do Congo', 'CD'),
(677, 'República Dominicana', 'DO'),
(680, 'República Pop. Dem. da Coreia', 'KP'),
(683, 'República Tcheca', 'CZ'),
(686, 'República Unida da Tanzânia', 'TZ'),
(689, 'Reunião', 'RE'),
(692, 'Romênia', 'RO'),
(695, 'Ruanda', 'RW'),
(698, 'Saara Ocidental', 'EH'),
(701, 'Saint Pierre e Miquelon', 'PM'),
(704, 'Samoa Americana', 'AS'),
(707, 'Samoa Ocidental', 'WS'),
(710, 'Santa Helena', 'SH'),
(713, 'Santa Lúcia', 'LC'),
(716, 'São Cristovão e Nevis', 'KN'),
(719, 'São Marino', 'SM'),
(722, 'São Tomé e Príncipe', 'ST'),
(725, 'São Vicente e Granadinas', 'VC'),
(728, 'Senegal', 'SN'),
(731, 'Serra Leoa', 'SL'),
(734, 'Sérvia', 'RS'),
(737, 'Seychelles', 'SC'),
(740, 'Singapura', 'SG'),
(743, 'Síria', 'SY'),
(746, 'Somália', 'SO'),
(749, 'Sri Lanka', 'LK'),
(752, 'Suazilândia', 'SZ'),
(755, 'Sudão', 'SD'),
(758, 'Suécia', 'SE'),
(761, 'Suíça', 'CH'),
(764, 'Suriname', 'SR'),
(767, 'Svalbard e Jan Mayen', 'SJ'),
(770, 'Tadjiquistão', 'TJ'),
(773, 'Tailândia', 'TH'),
(776, 'Taiwan', 'TW'),
(779, 'Terras Austrais Francesas', 'TF'),
(782, 'Territ.Britan.Oceano Índico', 'IO'),
(785, 'Território Ocupado Palestino', 'PS'),
(788, 'Timor-Leste', 'TL'),
(791, 'Togo', 'TG'),
(794, 'Tokelau', 'TK'),
(797, 'Tonga', 'TO'),
(800, 'Trinidad e Tobago', 'TT'),
(803, 'Tunísia', 'TN'),
(806, 'Turcomenistão', 'TM'),
(809, 'Turquia', 'TR'),
(812, 'Tuvalu', 'TV'),
(815, 'Ucrânia', 'UA'),
(818, 'Uganda', 'UG'),
(821, 'Uruguai', 'UY'),
(824, 'Uzbequistão', 'UZ'),
(827, 'Vanuatu', 'VU'),
(830, 'Vaticano', 'VA'),
(833, 'Venezuela', 'VE'),
(836, 'Vietnã', 'VN'),
(839, 'Yugoslávia', 'YU'),
(842, 'Zaire', 'ZR'),
(845, 'Zâmbia', 'ZM'),
(848, 'Zimbábue', 'ZW')
```
