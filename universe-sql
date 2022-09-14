--
-- PostgreSQL database dump
--

-- Dumped from database version 12.12 (Ubuntu 12.12-0ubuntu0.20.04.1)
-- Dumped by pg_dump version 12.12 (Ubuntu 12.12-0ubuntu0.20.04.1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: countries; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.countries (
    countries_id integer NOT NULL,
    name character varying NOT NULL,
    population_in_millions numeric
);


ALTER TABLE public.countries OWNER TO freecodecamp;

--
-- Name: countries_countries_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.countries_countries_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.countries_countries_id_seq OWNER TO freecodecamp;

--
-- Name: countries_countries_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.countries_countries_id_seq OWNED BY public.countries.countries_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(30) NOT NULL,
    discovered date,
    type character varying,
    shape character varying
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(30) NOT NULL,
    radius_in_km integer,
    discovered date,
    temperature_in_kelvins numeric,
    planet_id integer
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(30) NOT NULL,
    radius_in_km integer,
    habitable boolean NOT NULL,
    contains_liquid_water boolean,
    discovered date,
    star_id integer
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(30) NOT NULL,
    radius_in_km integer,
    star_types text,
    age_in_millions_of_years numeric,
    discovered date,
    galaxy_id integer
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: countries countries_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.countries ALTER COLUMN countries_id SET DEFAULT nextval('public.countries_countries_id_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: countries; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.countries VALUES (1, 'United Kingdom', 67.89);
INSERT INTO public.countries VALUES (2, 'France', 67.39);
INSERT INTO public.countries VALUES (3, 'Germany', 83.24);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', '1610-01-01', 'spiral', 'spiral');
INSERT INTO public.galaxy VALUES (2, 'Andromeda', '1924-12-30', 'spiral', 'spiral');
INSERT INTO public.galaxy VALUES (3, 'Canis Major dwarf galaxy', '2003-01-01', 'irregular', 'elliptical');
INSERT INTO public.galaxy VALUES (4, 'Cygnus A', '1939-01-01', 'radio galaxy', 'elliptical');
INSERT INTO public.galaxy VALUES (5, 'Messier 87', '1781-01-01', 'elliptical galaxy', 'elliptical');
INSERT INTO public.galaxy VALUES (6, 'Maffei 1', '1967-09-29', 'elliptical galaxy', 'elliptical');


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'The moon', 1737, '1610-01-07', 250, 1);
INSERT INTO public.moon VALUES (2, 'Titan', 2574, '1655-03-25', 93.7, 2);
INSERT INTO public.moon VALUES (3, 'Enceladus', 252, '1789-08-28', 75, 2);
INSERT INTO public.moon VALUES (4, 'Mimas', 198, '1789-09-17', 64, 2);
INSERT INTO public.moon VALUES (5, 'Dione', 561, '1684-03-30', 87, 2);
INSERT INTO public.moon VALUES (6, 'Tethys', 531, '1684-03-11', 86, 2);
INSERT INTO public.moon VALUES (7, 'Iapetus', 735, '1671-10-25', 110, 2);
INSERT INTO public.moon VALUES (8, 'Hyperion', 135, '1848-09-16', 93, 2);
INSERT INTO public.moon VALUES (9, 'Rhea', 764, '1672-12-23', 70, 2);
INSERT INTO public.moon VALUES (10, 'Europa', 1560, '1610-01-08', 102, 3);
INSERT INTO public.moon VALUES (11, 'Io', 1822, '1610-01-08', 110, 3);
INSERT INTO public.moon VALUES (12, 'Ganymede', 2634, '1610-01-07', 110, 3);
INSERT INTO public.moon VALUES (13, 'Callisto', 2410, '1610-01-07', 134, 3);
INSERT INTO public.moon VALUES (14, 'Telesto', 12, '1980-04-08', NULL, 3);
INSERT INTO public.moon VALUES (15, 'Epimetheus', 58, '1966-12-18', 78, 2);
INSERT INTO public.moon VALUES (16, 'Janus', 90, '1966-12-15', 76, 2);
INSERT INTO public.moon VALUES (17, 'Methone', 1, '2004-06-01', NULL, 2);
INSERT INTO public.moon VALUES (18, 'Fenrir', 2, '2005-05-04', NULL, 2);
INSERT INTO public.moon VALUES (19, 'Oberon', 761, '1787-01-11', 75, 7);
INSERT INTO public.moon VALUES (20, 'Titania', 788, '1787-01-11', 70, 7);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Earth', 6371, true, true, '0240-01-01 BC', 1);
INSERT INTO public.planet VALUES (2, 'Saturn', 58232, false, false, '1610-01-01', 1);
INSERT INTO public.planet VALUES (3, 'Jupiter', 69911, false, false, '1610-01-01', 1);
INSERT INTO public.planet VALUES (4, 'Mercury', 2440, false, false, '1631-01-01', 1);
INSERT INTO public.planet VALUES (5, 'Venus', 6052, false, false, '1610-08-01', 1);
INSERT INTO public.planet VALUES (6, 'Mars', 3390, false, true, '1610-08-01', 1);
INSERT INTO public.planet VALUES (7, 'Uranus', 25362, false, false, '1781-03-17', 1);
INSERT INTO public.planet VALUES (8, 'Neptune', 24622, false, false, '1846-09-23', 1);
INSERT INTO public.planet VALUES (9, 'HR 8799 e', 85790, false, false, '2010-11-01', 3);
INSERT INTO public.planet VALUES (13, 'HR 8799 b', 85790, false, false, '2008-11-13', 3);
INSERT INTO public.planet VALUES (10, 'HR 8799 d', 85790, false, false, '2008-11-13', 3);
INSERT INTO public.planet VALUES (12, 'HR 8799 c', 92939, false, false, '2008-11-13', 3);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'The Sun', 695000, 'G2V', 4600, '1609-01-01', 1);
INSERT INTO public.star VALUES (2, 'P Cygni', 52870000, 'LBV', NULL, '1600-08-18', 1);
INSERT INTO public.star VALUES (3, 'HR 8799', 932000, 'A5 V', 60, '2008-11-13', 1);
INSERT INTO public.star VALUES (4, 'Alpheratz', 1878000, 'B9p', 60, '1781-07-21', 2);
INSERT INTO public.star VALUES (6, 'Antares', 4730000, 'M1.5Iab-Ib', 11, '1819-04-13', 1);
INSERT INTO public.star VALUES (7, 'Betelgeuse', 6170000, 'M1-2', 10, '1836-01-01', 1);


--
-- Name: countries_countries_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.countries_countries_id_seq', 3, true);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 6, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 20, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 13, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 7, true);


--
-- Name: countries countries_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.countries
    ADD CONSTRAINT countries_pkey PRIMARY KEY (countries_id);


--
-- Name: countries countries_unique; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.countries
    ADD CONSTRAINT countries_unique UNIQUE (countries_id);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: galaxy galaxy_unique; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_unique UNIQUE (galaxy_id);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: moon moon_unique; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_unique UNIQUE (moon_id);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: planet planet_unique; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_unique UNIQUE (planet_id);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: star star_unique; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_unique UNIQUE (star_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

