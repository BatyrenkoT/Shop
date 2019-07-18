--
-- PostgreSQL database dump
--

-- Dumped from database version 9.4.23
-- Dumped by pg_dump version 9.4.23
-- Started on 2019-07-18 19:39:57

SET statement_timeout = 0;
SET lock_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;

--
-- TOC entry 1 (class 3079 OID 11855)
-- Name: plpgsql; Type: EXTENSION; Schema: -; Owner: 
--

CREATE EXTENSION IF NOT EXISTS plpgsql WITH SCHEMA pg_catalog;


--
-- TOC entry 2069 (class 0 OID 0)
-- Dependencies: 1
-- Name: EXTENSION plpgsql; Type: COMMENT; Schema: -; Owner: 
--

COMMENT ON EXTENSION plpgsql IS 'PL/pgSQL procedural language';


SET default_tablespace = '';

SET default_with_oids = false;

--
-- TOC entry 173 (class 1259 OID 57375)
-- Name: city; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.city (
    id integer NOT NULL,
    name character varying NOT NULL,
    country_id integer NOT NULL
);


ALTER TABLE public.city OWNER TO postgres;

--
-- TOC entry 174 (class 1259 OID 57381)
-- Name: country; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.country (
    id integer NOT NULL,
    name character varying NOT NULL
);


ALTER TABLE public.country OWNER TO postgres;

--
-- TOC entry 175 (class 1259 OID 57387)
-- Name: customer; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.customer (
    id integer NOT NULL,
    person_id integer NOT NULL
);


ALTER TABLE public.customer OWNER TO postgres;

--
-- TOC entry 176 (class 1259 OID 57390)
-- Name: employee; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.employee (
    id integer NOT NULL,
    person_id integer NOT NULL,
    hire_date date NOT NULL,
    director_id integer,
    notes text
);


ALTER TABLE public.employee OWNER TO postgres;

--
-- TOC entry 177 (class 1259 OID 57396)
-- Name: kind; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.kind (
    id integer NOT NULL,
    name character varying NOT NULL
);


ALTER TABLE public.kind OWNER TO postgres;

--
-- TOC entry 178 (class 1259 OID 57402)
-- Name: order_details; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.order_details (
    orders_id integer NOT NULL,
    product_id integer NOT NULL,
    quantity double precision NOT NULL,
    price money NOT NULL
);


ALTER TABLE public.order_details OWNER TO postgres;

--
-- TOC entry 179 (class 1259 OID 57405)
-- Name: orders; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.orders (
    id integer NOT NULL,
    ship_date date NOT NULL,
    receive_date date NOT NULL,
    customer_id integer NOT NULL,
    employee_id integer NOT NULL
);


ALTER TABLE public.orders OWNER TO postgres;

--
-- TOC entry 180 (class 1259 OID 57408)
-- Name: person; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.person (
    id integer NOT NULL,
    first_name character varying NOT NULL,
    last_name character varying NOT NULL,
    date_birth date NOT NULL,
    city_id integer NOT NULL
);


ALTER TABLE public.person OWNER TO postgres;

--
-- TOC entry 181 (class 1259 OID 57414)
-- Name: product; Type: TABLE; Schema: public; Owner: postgres; Tablespace: 
--

CREATE TABLE public.product (
    id integer NOT NULL,
    name character varying NOT NULL,
    price money NOT NULL,
    kind_id integer NOT NULL,
    country_id integer NOT NULL
);


ALTER TABLE public.product OWNER TO postgres;

--
-- TOC entry 2052 (class 0 OID 57375)
-- Dependencies: 173
-- Data for Name: city; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.city (id, name, country_id) FROM stdin;
1	Madrid	1
2	Paris	2
3	London	3
4	Kyiv	4
5	Berlin	5
6	Moscow	6
7	Rome	7
8	Tokio	8
9	Beijing 	9
10	New Delhi 	10
11	Brazil\n	11
12	Buenos Aires 	12
13	Washington	13
14	Oslo 	14
15	Stockholm 	15
16	Mexico 	16
17	Ottawa 	17
18	Kampala 	18
19	Australia	19
20	Wellington 	20
21	Koror	21
22	Copenhagen 	22
23	Ankara 	23
24	Cairo 	24
25	Belgrade 	25
26	Tehran 	26
27	Baghdad 	27
28	Jerusalem	28
29	Lima 	29
30	Chili	30
31	Amsterdam	31
32	Andorra la Vella 	32
33	T'bilisi 	33
34	Warsaw 	34
35	Bangkok 	35
36	Brussels 	36
37	Helsinki 	37
38	Budapest 	38
39	Vienna 	39
40	Dublin 	40
41	Kabul 	41
42	Tirana 	42
43	Algiers 	43
44	Pago Pago 	44
45	Andorra la Vella 	45
46	Luanda 	46
47	The Valley 	47
48	Saint John's 	48
49	Yerevan 	49
50	Oranjestad 	50
51	Manama 	51
52	Dhaka 	52
53	Bridgetown 	53
54	Minsk 	54
55	Brussels 	55
56	Belmopan 	56
57	Porto-Novo	57
58	Hamilton 	58
59	Thimphu 	59
60	La Paz	60
61	Sarajevo 	61
62	Gaborone 	62
63	Road Town 	63
64	Bandar Seri Begawan 	64
65	Sofia 	65
66	Ouagadougou 	66
67	Rangoon	67
68	Bujumbura 	68
69	Phnom Penh 	69
70	Yaounde 	70
71	Bangui 	71
72	N'Djamena 	72
73	Santiago 	73
74	The Settlement 	74
75	West Island 	75
76	Bogota 	76
77	Moroni 	77
78	San Jose 	78
79	Havana 	79
80	Nicosia 	80
\.


--
-- TOC entry 2053 (class 0 OID 57381)
-- Dependencies: 174
-- Data for Name: country; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.country (id, name) FROM stdin;
1	Spain
2	France
3	England
4	Ukraine
5	Germany
6	Russia
7	Italy
8	Japan
9	China
10	India
11	Brazil
12	Argentina
13	USA
14	Norway
15	Sweden
16	Mexico
17	Canada
18	Uganda
19	Australia
20	New Zealand
22	Denmark 
23	Turkey
24	Egypt
25	Montenegro
26	Iran
27	Iraq
28	Israel
29	Peru
30	Chili
31	Netherlands
37	Finland
38	Hungary
39	Austria
40	Ireland
41	Afghanistan 
42	Albania 
43	Algeria 
44	American Samoa 
45	Andorra 
46	Angola 
47	Anguilla 
48	Antigua and Barbuda 
49	Armenia 
50	Aruba 
51	Bahrain 
52	Bangladesh 
53	Barbados
54	Belarus
55	Belgium 
56	Belize
57	Benin 
58	Bermuda 
59	Bhutan 
60	Bolivia 
61	Bosnia and Herzegovina 
62	Botswana 
63	Brunei 
64	Burkina Faso 
65	Burma 
66	Burundi 
67	Cambodia 
68	Cameroon 
69	Cape Verde 
70	Cayman Islands 
71	Central African Republic 
72	Chad 
73	Chile
74	Christmas Island 
75	Colombia 
76	Comoros 
77	Congo
78	Costa Rica 
79	Cuba 
80	Cyprus 
21	Palau
32	Andorra 
33	Georgia 
34	Poland 
35	Thailand 
36	Belgium 
\.


--
-- TOC entry 2054 (class 0 OID 57387)
-- Dependencies: 175
-- Data for Name: customer; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.customer (id, person_id) FROM stdin;
1	1
3	3
27	27
28	28
29	29
30	30
31	31
32	32
33	33
34	34
35	35
36	36
37	37
38	38
39	39
40	40
2	2
4	4
5	5
6	6
7	7
8	8
9	9
10	10
11	11
12	12
13	13
14	14
15	15
16	16
17	17
18	18
19	19
20	20
21	21
22	22
23	23
24	24
25	25
26	26
\.


--
-- TOC entry 2055 (class 0 OID 57390)
-- Dependencies: 176
-- Data for Name: employee; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.employee (id, person_id, hire_date, director_id, notes) FROM stdin;
1	41	1993-07-11	\N	director1
2	42	1993-07-22	\N	director2
3	43	1993-07-22	\N	director3
4	44	1993-07-22	1	\N
6	46	1993-07-22	3	\N
7	47	1993-07-22	1	\N
8	48	1993-07-22	2	\N
10	50	1993-07-22	1	\N
11	51	1993-08-15	2	\N
13	53	1993-08-15	1	\N
14	54	1993-08-15	2	\N
15	55	1993-08-15	3	\N
16	56	1993-08-15	1	\N
17	57	1993-08-15	2	\N
18	58	1993-08-15	3	\N
19	59	1993-08-15	1	\N
20	60	1993-08-15	2	\N
21	61	2001-07-15	3	\N
22	62	2001-07-15	1	\N
23	63	2001-07-15	2	\N
24	64	2001-07-15	3	\N
25	65	2001-07-15	1	\N
26	66	2001-07-15	2	\N
27	67	2001-07-15	3	\N
28	68	2001-07-15	1	\N
29	69	2001-07-15	2	\N
30	70	2001-08-23	3	\N
31	71	2001-08-23	1	\N
5	45	1993-07-22	2	\N
9	49	1993-07-22	3	\N
12	52	1993-08-15	3	\N
32	72	2001-08-23	2	\N
33	73	2001-08-23	3	\N
34	74	2001-08-23	1	\N
35	75	2001-08-23	2	\N
36	76	2001-08-23	3	\N
37	77	2001-08-23	1	\N
38	78	2001-08-23	2	\N
39	79	2001-08-23	3	\N
40	80	2003-06-06	1	\N
\.


--
-- TOC entry 2056 (class 0 OID 57396)
-- Dependencies: 177
-- Data for Name: kind; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.kind (id, name) FROM stdin;
1	Domestic 
2	Non-domestic 
\.


--
-- TOC entry 2057 (class 0 OID 57402)
-- Dependencies: 178
-- Data for Name: order_details; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.order_details (orders_id, product_id, quantity, price) FROM stdin;
1	1	4	10,00?
2	2	3	15,00?
3	3	4	10,00?
4	4	5	9,00?
5	5	13	20,00?
6	6	11	5,00?
7	7	13	4,00?
8	8	11	1,00?
1	9	11	2,00?
1	3	2	2,00?
1	5	3	3,00?
3	2	2	1,00?
3	3	3	3,00?
3	5	6	2,00?
4	5	6	2,00?
4	10	6	2,00?
4	12	6	2,00?
4	15	6	2,00?
4	30	6	2,00?
4	42	6	2,00?
4	45	6	2,00?
4	47	6	2,00?
4	80	6	2,00?
4	75	6	2,00?
4	32	6	2,00?
6	22	1	5,00?
6	24	10	5,00?
6	14	21	5,00?
6	63	2	5,00?
6	34	20	2,00?
22	3	10	3,00?
22	5	10	3,00?
22	6	10	3,00?
22	8	11	3,00?
22	17	4	5,00?
22	23	1	4,00?
22	5	67	23,00?
54	31	5	13,00?
54	4	50	14,00?
54	4	67	1,00?
80	5	23	31,00?
10	13	13	5,00?
4	11	52	51,00?
5	2	4	3,00?
15	12	14	13,00?
22	22	2	2,00?
1	13	23	2,00?
15	23	5	3,00?
15	2	45	7,00?
16	2	15	7,00?
23	21	5	7,00?
23	21	5	17,00?
14	2	11	3,00?
15	21	4	6,00?
1	42	5	8,00?
11	2	15	58,00?
17	21	2	5,00?
17	10	5	1,00?
51	2	2	26,00?
32	1	6	47,00?
11	12	61	47,00?
31	22	51	1,00?
13	15	6	7,00?
19	3	5	2,00?
29	30	51	2,00?
25	30	53	21,00?
25	2	5	3,00?
11	4	23	1,00?
71	24	54	1,00?
42	32	5	3,00?
23	32	4	3,00?
64	12	14	23,00?
42	13	2	4,00?
9	23	24	4,00?
1	2	1	4,00?
1	1	10	4,00?
1	3	10	4,00?
5	40	10	4,00?
7	5	23	4,00?
6	66	66	66,00?
\.


--
-- TOC entry 2058 (class 0 OID 57405)
-- Dependencies: 179
-- Data for Name: orders; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.orders (id, ship_date, receive_date, customer_id, employee_id) FROM stdin;
1	2019-08-01	2019-08-11	1	1
2	2019-08-02	2019-08-12	2	2
3	2019-08-03	2019-08-13	3	3
4	2019-08-04	2019-08-14	4	4
5	2019-08-05	2019-08-15	5	5
6	2019-08-06	2019-08-16	6	6
7	2019-08-07	2019-08-17	7	7
8	2019-08-09	2019-08-19	8	8
9	2019-08-08	2019-08-18	9	9
10	2019-08-10	2019-08-20	10	10
11	2019-06-11	2019-06-21	11	11
12	2019-06-12	2019-06-22	12	12
13	2019-06-13	2019-06-23	13	13
14	2019-06-14	2019-06-24	14	14
15	2019-06-15	2019-06-25	15	15
16	2019-06-16	2019-06-26	16	16
17	2019-06-17	2019-06-27	17	17
18	2019-06-18	2019-06-28	18	18
19	2019-06-19	2019-06-29	19	19
20	2019-06-20	2019-06-30	20	20
21	2019-01-01	2019-02-01	21	21
22	2019-02-01	2019-03-01	22	22
23	2019-03-01	2019-04-01	23	23
24	2019-04-01	2019-05-01	24	24
25	2019-05-01	2019-06-01	25	25
26	2019-06-01	2019-07-01	26	26
27	2019-07-01	2019-07-01	27	27
28	2019-08-01	2019-08-01	28	28
29	2019-09-01	2019-10-01	29	29
30	2019-10-01	2019-11-01	30	30
31	2011-11-11	2011-11-21	31	31
32	2012-12-22	2013-01-02	32	32
33	2013-03-13	2013-04-23	33	33
34	2014-04-14	2014-04-24	34	34
35	2015-05-25	2015-06-04	35	35
36	2016-06-06	2016-06-16	36	36
37	2007-06-06	2016-07-06	37	37
38	2009-01-21	2009-02-23	38	38
39	2000-04-21	2001-01-01	39	39
40	2014-05-24	2014-05-30	40	40
60	2010-01-01	2009-01-25	20	20
61	2014-03-04	2014-04-04	21	21
62	2014-03-05	2014-04-04	22	22
63	2014-03-07	2014-04-07	23	23
64	2014-03-08	2014-04-08	24	24
65	2014-03-14	2014-03-24	25	25
66	2014-03-24	2014-03-30	26	26
67	2014-03-13	2014-05-13	27	27
68	2014-03-01	2014-03-21	28	28
69	2014-07-17	2014-08-13	29	29
70	2017-06-26	2017-07-26	30	30
71	2017-06-16	2017-06-26	31	31
72	2017-03-01	2017-03-30	32	32
73	2018-05-13	2018-05-27	33	33
74	2018-05-17	2018-06-17	34	34
75	2018-05-19	2018-06-19	35	35
76	2018-05-21	2018-07-02	36	36
77	2018-05-04	2018-05-31	37	37
78	2018-05-01	2018-06-04	38	38
79	2018-05-19	2018-07-10	39	39
80	2018-08-13	2018-08-30	40	40
41	2011-05-14	2011-05-24	1	1
42	2011-05-14	2011-05-24	2	2
43	2011-05-14	2011-05-24	3	3
44	2011-03-10	2011-03-20	4	4
45	2011-03-10	2011-03-20	5	5
46	2011-03-10	2011-03-20	6	6
47	2011-10-03	2011-10-13	7	7
48	2011-10-03	2011-10-13	8	8
49	2011-10-03	2011-10-13	9	9
50	2011-10-03	2011-10-13	10	10
51	2001-01-01	2001-02-01	11	11
52	2002-01-01	2002-02-01	12	12
53	2003-01-01	2003-03-01	13	13
54	2004-01-01	2004-04-01	14	14
55	2005-01-01	2005-05-01	15	15
56	2006-01-01	2007-02-01	16	16
57	2007-01-01	2007-02-02	17	17
58	2008-01-01	2008-03-01	18	18
59	2009-01-01	2009-01-20	19	19
\.


--
-- TOC entry 2059 (class 0 OID 57408)
-- Dependencies: 180
-- Data for Name: person; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.person (id, first_name, last_name, date_birth, city_id) FROM stdin;
1	Iryna\n	Lutska	1999-06-30	1
2	Vlad	Skakun	2001-05-29	2
3	Dima	Stefurak	1999-03-11	3
4	Yana	Kushniryk	1999-04-23	4
5	Yulia	Apetroy	2000-11-10	5
12	Pavlo	Rachukov	1998-07-07	12
41	Sasha	Lysko	1998-06-20	41
42	Oksana	Hrytsyak	1969-02-10	42
43	Ariana	Grande	1990-12-14	43
44	Mykhailo	Kruchkov	1997-06-22	44
45	Olena	Kuz	1996-11-29	45
46	Sandra	Barabanova	2000-12-13	46
47	Jessy	Pinkman	1989-03-03	47
48	Elina	Lisko	1960-09-16	48
49	Maryna	Lisova	1950-04-01	49
50	Dmytro	Scherbakov	1999-05-12	50
51	Alisa	Abdurohmanovma	1970-01-01	51
52	Vitalii	Hrublyak	1997-01-01	52
53	Anton	Harasymchuk	1995-05-09	53
54	Oleksandra	Horetska	1997-11-02	54
55	Nikol	Rozumna	2001-01-09	55
56	Ivan	Ivanov	1975-12-31	56
57	Petro	Petrovchuk	1960-07-01	57
58	Vasyl	Vasylenko	1979-09-12	58
59	Pavlo	Pavlenko	1986-09-14	59
60	Taras	Tarasenko	1990-08-19	60
61	Anastasiia	Homeniuk	1999-07-01	61
62	Yana	Spynul	1998-10-10	62
63	Valeriia	Straton	1999-03-04	63
64	Yulia	Havryliuk	1999-04-12	64
65	Ksenia	Branashko	1999-09-12	65
66	Yulia	Kosovan	1999-03-09	66
67	Pavlo	Dranchuk	1998-09-07	67
68	Artur	Tomniuk	1999-04-10	68
69	Petro	Koleschuk	1999-12-20	69
70	Denys	Pidlubnii	1999-08-12	70
71	Denys	Petrov	1980-12-02	71
72	Lena	Holovach	1981-09-13	72
73	Valerii	Zhmyshenko	1965-02-14	73
74	Gabe	Newell	1960-02-14	74
75	Hideo	Kojima	1963-08-24	75
76	Sun	Chan	1983-06-12	76
77	Jessica	Barter	1987-07-07	77
78	Jung	Lee	1993-11-11	78
79	Pellek	Leen	1990-12-16	79
80	Mariia	Way	1992-08-25	80
6	Vasyl	Hulei	1998-07-09	6
7	Andrii	Kyrstuk	1998-01-07	7
8	Anna	Melnuchyk	1988-07-07	8
9	Vita	Stelmax	19988-07-15	9
10	Nadia	Annych	1998-07-31	10
11	Yana	Kosol	1995-02-11	11
13	Vlad	Mahalevych	1978-03-01	13
14	Natalia	Romanenko	1979-12-10	14
15	Yura	Lucuk	1989-04-23	15
16	Vasil	Zaporonyk	1994-05-13	16
17	Nelia	Sakalosh	1990-02-09	17
18	Alina	Hurak	1998-07-09	18
19	Anna	Rotary	1998-07-10	19
20	Natalia	Doblryanska\n	1998-07-11	20
21	Nastya	Har	1998-07-12	21
22	Tania	Diachuk	1998-07-13	22
23	Vadim	Striha	1998-07-14	23
24	Rostik	Boiko	1998-07-15	24
25	Iryna	Lialchuk	1998-07-16	25
26	Sashka	Hrublak	1998-07-17	26
27	Christyna	Tsyganovich	1998-07-18	27
28	Daryna	Rai	1998-07-19	28
29	Andrii	Ryabui	1998-07-20	29
30	Julia	Danilova	1998-07-21	30
31	Olia	Havrulyk	1998-07-22	31
32	Marta	Husa	1998-07-23	32
33	Max	Voronin	1998-07-24	33
34	Stas	Yazlovetskii	1998-07-25	34
35	Toni	Stark	1998-07-26	35
36	Tanya	Boiko	1998-07-27	36
37	Dima	Stratiichuk	1998-08-07	37
38	Oleg	Danulenko	1998-08-01	38
39	Halyna	Hus	1998-08-03	39
40	Ira	Dokal	1998-08-02	40
\.


--
-- TOC entry 2060 (class 0 OID 57414)
-- Dependencies: 181
-- Data for Name: product; Type: TABLE DATA; Schema: public; Owner: postgres
--

COPY public.product (id, name, price, kind_id, country_id) FROM stdin;
2	Apricot 	10,00?	1	2
3	Pineapple 	15,00?	1	4
4	Orange 	22,00?	1	3
5	Watermelon 	35,00?	1	5
6	Banana 	32,00?	2	6
7	Mutton 	56,00?	2	7
8	Pancake 	23,00?	2	8
9	Wafer 	52,00?	2	3
10	Vermicelli 	11,00?	2	9
11	Ham 	8,00?	1	10
12	Grape 	6,00?	1	23
13	Cherry 	4,00?	1	21
14	Water 	3,00?	1	25
15	Beef 	2,00?	1	75
16	Pea 	32,00?	2	11
17	Pomegranate 	60,00?	2	23
18	Grapefruit 	32,00?	2	43
19	Mushroom 	123,00?	2	76
20	Pear 	55,00?	2	76
21	Yeast 	32,00?	1	23
22	Melon 	5,00?	1	10
23	Gelatin	2,00?	1	65
24	Grease 	12,00?	1	5
25	Yoghurt 	50,00?	1	6
26	Cocoa 	4,00?	2	7
27	Squid 	21,00?	2	8
28	Cabbage 	41,00?	2	9
29	Potato 	45,00?	2	11
30	Porridge 	23,00?	1	15
31	Kvass 	26,00?	1	73
32	Kefir 	234,00?	1	17
33	Strawberry 	43,00?	1	27
34	Cranberry 	21,00?	1	67
35	Sausage 	47,00?	2	47
36	Sweet 	25,00?	2	57
37	Coffee 	27,00?	2	54
38	Crab 	12,00?	2	69
39	Starch 	1,00?	2	52
40	Shrimp 	14,00?	1	63
41	Cereals 	11,00?	1	42
42	Yoghurt 	25,00?	1	42
43	Cocoa 	86,00?	1	13
44	Grape 	32,00?	1	41
45	Orange 	13,00?	1	31
46	Vermicelli 	26,00?	1	63
47	Grape 	73,00?	1	23
48	Orange 	15,00?	1	52
49	Vermicelli 	65,00?	1	22
50	Pancake 	58,00?	2	23
51	Grape 	24,00?	2	78
52	Orange 	42,00?	2	74
53	Pancake 	42,00?	2	54
54	Pancake 	26,00?	2	55
55	Orange 	32,00?	2	55
56	Tofu	15,00?	2	33
57	Cocoa 	25,00?	2	22
58	Macaroni 	14,00?	2	11
59	Tofu	14,00?	2	63
60	Soda 	43,00?	1	2
61	Mayonnaise 	33,00?	2	4
62	Tofu	32,00?	1	3
63	Coffee 	32,00?	2	76
64	Tofu	16,00?	1	6
65	Watermelon 	18,00?	2	4
66	Coffee 	23,00?	1	7
67	Tofu	16,00?	2	8
68	Watermelon 	18,00?	1	9
69	Pea 	50,00?	2	10
70	Watermelon 	12,00?	1	53
71	Tofu	235,00?	2	11
72	Pomegranate 	23,00?	2	20
73	Tofu	24,00?	2	31
74	Pomegranate 	12,00?	1	30
75	Tofu	10,00?	1	40
76	Pea 	32,00?	1	50
77	Grapefruit	13,00?	1	60
78	Tofu	25,00?	2	68
79	Grapefruit	74,00?	2	25
80	Pea 	23,00?	1	66
1	Tofu	20,00?	1	1
81	milk	23,00?	1	20
82	milk	23,00?	2	3
\.


--
-- TOC entry 1918 (class 2606 OID 57421)
-- Name: city_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.city
    ADD CONSTRAINT city_pkey PRIMARY KEY (id);


--
-- TOC entry 1920 (class 2606 OID 57423)
-- Name: country_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.country
    ADD CONSTRAINT country_pkey PRIMARY KEY (id);


--
-- TOC entry 1922 (class 2606 OID 57425)
-- Name: customer_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.customer
    ADD CONSTRAINT customer_pkey PRIMARY KEY (id);


--
-- TOC entry 1924 (class 2606 OID 57427)
-- Name: employee_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.employee
    ADD CONSTRAINT employee_pkey PRIMARY KEY (id);


--
-- TOC entry 1926 (class 2606 OID 57429)
-- Name: kind_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.kind
    ADD CONSTRAINT kind_pkey PRIMARY KEY (id);


--
-- TOC entry 1928 (class 2606 OID 57431)
-- Name: orders_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.orders
    ADD CONSTRAINT orders_pkey PRIMARY KEY (id);


--
-- TOC entry 1930 (class 2606 OID 57433)
-- Name: person_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.person
    ADD CONSTRAINT person_pkey PRIMARY KEY (id);


--
-- TOC entry 1932 (class 2606 OID 57435)
-- Name: product_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres; Tablespace: 
--

ALTER TABLE ONLY public.product
    ADD CONSTRAINT product_pkey PRIMARY KEY (id);


--
-- TOC entry 1933 (class 2606 OID 57436)
-- Name: city_country_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.city
    ADD CONSTRAINT city_country_id_fkey FOREIGN KEY (country_id) REFERENCES public.country(id);


--
-- TOC entry 1934 (class 2606 OID 57441)
-- Name: customer_person_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.customer
    ADD CONSTRAINT customer_person_id_fkey FOREIGN KEY (person_id) REFERENCES public.person(id);


--
-- TOC entry 1935 (class 2606 OID 57446)
-- Name: employee_person_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.employee
    ADD CONSTRAINT employee_person_id_fkey FOREIGN KEY (person_id) REFERENCES public.person(id);


--
-- TOC entry 1936 (class 2606 OID 57451)
-- Name: order_details_orders_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.order_details
    ADD CONSTRAINT order_details_orders_id_fkey FOREIGN KEY (orders_id) REFERENCES public.orders(id);


--
-- TOC entry 1937 (class 2606 OID 57456)
-- Name: order_details_product_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.order_details
    ADD CONSTRAINT order_details_product_id_fkey FOREIGN KEY (product_id) REFERENCES public.product(id);


--
-- TOC entry 1938 (class 2606 OID 57461)
-- Name: orders_customer_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.orders
    ADD CONSTRAINT orders_customer_id_fkey FOREIGN KEY (customer_id) REFERENCES public.customer(id);


--
-- TOC entry 1939 (class 2606 OID 57466)
-- Name: orders_employee_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.orders
    ADD CONSTRAINT orders_employee_id_fkey FOREIGN KEY (employee_id) REFERENCES public.employee(id);


--
-- TOC entry 1940 (class 2606 OID 57471)
-- Name: person_city_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.person
    ADD CONSTRAINT person_city_id_fkey FOREIGN KEY (city_id) REFERENCES public.city(id);


--
-- TOC entry 1941 (class 2606 OID 57476)
-- Name: product_country_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.product
    ADD CONSTRAINT product_country_id_fkey FOREIGN KEY (country_id) REFERENCES public.country(id);


--
-- TOC entry 1942 (class 2606 OID 57481)
-- Name: product_kind_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.product
    ADD CONSTRAINT product_kind_id_fkey FOREIGN KEY (kind_id) REFERENCES public.kind(id);


--
-- TOC entry 2068 (class 0 OID 0)
-- Dependencies: 6
-- Name: SCHEMA public; Type: ACL; Schema: -; Owner: postgres
--

REVOKE ALL ON SCHEMA public FROM PUBLIC;
REVOKE ALL ON SCHEMA public FROM postgres;
GRANT ALL ON SCHEMA public TO postgres;
GRANT ALL ON SCHEMA public TO PUBLIC;


-- Completed on 2019-07-18 19:39:57

--
-- PostgreSQL database dump complete
--

