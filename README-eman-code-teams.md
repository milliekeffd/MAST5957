# MAST5957
Year in data project 
---
title: "GapminderRMD"
author: "Emmanuel Richter"
date: "01/03/2022"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

Installing Packages
```{r}
install.packages("gapminder")
library(gapminder)
install.packages("ggplot2")
library(ggplot2)
install.packages("tidyverse")
library(tidyverse)
install.packages("scales")
library(scales)
```{r}
#Checking dataset
gapminder<-gapminder
head(gapminder)
dim(gapminder)

#Looking for missing values
sum(is.na(gapminder))

#Summary
summary(gapminder)

unique(gapminder$year)
```
GDP per Capita by Continent (bar charts)
```{r}
#GDP per Capita by Continent 

#1957
GDP1952 <- filter(gapminder, year == 1952)

ggplot(GDP1952, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1952")+ scale_y_continuous(labels = comma)


#1957
GDP1957 <- filter(gapminder, year == 1957)

ggplot(GDP1957, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1957")+ scale_y_continuous(labels = comma)


#1962
GDP1962 <- filter(gapminder, year == 1962)

ggplot(GDP1962, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1962")+ scale_y_continuous(labels = comma)


#1967
GDP1967 <- filter(gapminder, year == 1967)

ggplot(GDP1967, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1967")+ scale_y_continuous(labels = comma)


#1972
GDP1972 <- filter(gapminder, year == 1972)

ggplot(GDP1972, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1972")+ scale_y_continuous(labels = comma)


#1977
GDP1977 <- filter(gapminder, year == 1977)

ggplot(GDP1977, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1977")+ scale_y_continuous(labels = comma)


#1982
GDP1982<-filter(gapminder,year==1982)

ggplot(GDP1982, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1982")+ scale_y_continuous(labels = comma)


#1987
GDP1987<-filter(gapminder,year==1987)

ggplot(GDP1982, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1987")+ scale_y_continuous(labels = comma)


#1992
GDP1992<-filter(gapminder,year==1992)

ggplot(GDP1992, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1992")+ scale_y_continuous(labels = comma)


#1997
GDP1997<-filter(gapminder,year==1997)

ggplot(GDP1997, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 1997")+ scale_y_continuous(labels = comma)


#2002
GDP2002<-filter(gapminder,year==2002)

ggplot(GDP2002, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 2002")+ scale_y_continuous(labels = comma)


#2007
GDP2007<-filter(gapminder,year==2007)

ggplot(GDP2007, aes(x=continent, y=gdpPercap,fill=continent)) + geom_bar(stat = "identity") +
  xlab("Continents") +
  ylab("GDP per Capita") +
  ggtitle("GDP Per Capita by Contienent 2007") + scale_y_continuous(labels = comma) 

```

GDP per Capita by Continent (Box plot)
```{r}
#1952
ggplot(GDP1952, aes(x=continent, y=gdpPercap,fill=continent)) + 
  geom_boxplot()+labs(title="GDP per cap by Continent 1952")

```


Comparing Life Expectancy with Gdp per cap
```{r}
#Comparing Life Expectancy with Gdp per cap

#Overall Dataset
ggplot(gapminder, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point()

#1952 

ggplot(GDP1952, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1952")+ scale_y_continuous(labels = comma)


#1957
ggplot(GDP1957, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1957")+ scale_y_continuous(labels = comma)


#1962
ggplot(GDP1962, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1962")+ scale_y_continuous(labels = comma)


#1967
ggplot(GDP1967, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1967")+ scale_y_continuous(labels = comma)


#1972
ggplot(GDP1972, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1972")+ scale_y_continuous(labels = comma)


#1977
ggplot(GDP1977, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1977")+ scale_y_continuous(labels = comma)


#1982
ggplot(GDP1982, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1982")+ scale_y_continuous(labels = comma)


#1987
ggplot(GDP1987, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1987")+ scale_y_continuous(labels = comma)


#1992
ggplot(GDP1992, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1992")+ scale_y_continuous(labels = comma)


#1997
ggplot(GDP1997, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 1997")+ scale_y_continuous(labels = comma)


#2002
ggplot(GDP2002, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 2002")+ scale_y_continuous(labels = comma)


#2007
ggplot(GDP2007, aes(x = lifeExp, y = gdpPercap, color = continent)) + 
  geom_point() +
  ggtitle("GDP Per Capita by Life Expectancy 2007")+ scale_y_continuous(labels = comma)
