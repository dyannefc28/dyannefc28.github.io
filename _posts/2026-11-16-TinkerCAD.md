---
layout: post
title: Basic Traffic Light Circuit in TinkerCAD
image: "/posts/Traffic-Light.png"
tags: [TinkerCAD]
---


The goal of this project is to build a Basic Traffic light system in TinkerCAD. 

This includes modifying basic circuit to add additional functionality such as pedestrian crossing. 

___

This is the code I used: 

```
// C++ code
//
//Variables
int NSGreen = 2; //Attaches north/south green variable to pin two
int NSYellow = 4; //Attaches north/south yellow variable to pin four
int NSRed = 6; //Attaches north/south red variable to pin six
int EWGreen = 3; //Attaches east/west green variable to pin three
int EWYellow = 5; //Attaches east/west yellow variable to pin five
int EWRed = 7; //Attaches east/west red variable to pin seven

void setup() {
  // put your setup code here, to run once:
  pinMode ( NSGreen, OUTPUT ); //Sets pin mode for north/south green
  pinMode ( NSYellow, OUTPUT ); //Sets pin mode for north/south yellow
  pinMode ( NSRed, OUTPUT ); //Sets pin mode for north/south red
  pinMode ( EWGreen, OUTPUT ); //Sets pin mode for east/west green
  pinMode ( EWYellow, OUTPUT ); //Sets pin mode for east/west yellow
  pinMode ( EWRed, OUTPUT ); //Sets pin mode for east/west red
  //For this circuit setting a pin high turns the LED OFF, and low turns the LED ON
  digitalWrite ( NSGreen, HIGH ); //Sets default state for north/south green on first pass
  digitalWrite ( NSYellow, HIGH ); //Sets default state for north/south yellow on first pass
  digitalWrite ( EWGreen, HIGH ); //Sets default state for east/west green on first pass
  digitalWrite ( EWYellow, HIGH ); //Sets default state for  east/west yellow on first pass
}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite ( NSRed, LOW ); //Turn on north/south red
  digitalWrite ( EWRed, LOW ); //Turn on east/west red
  delay ( 3000 ); //Wait 3 seconds or 3000 milli seconds
  digitalWrite ( NSRed, HIGH ); //Turn off north/south red
  digitalWrite ( NSGreen, LOW ); //Turn on north/south green
  delay ( 3000 ); //Wait 3 seconds or 3000 milli seconds
  digitalWrite ( NSGreen, HIGH ); //Turn off north/south green
  digitalWrite ( NSYellow, LOW ); //Turn on north/south yellow
  delay ( 2000 ); //Wait 2 seconds or 2000 milli seconds
  digitalWrite ( NSYellow, HIGH); //Turn off north/south yellow
  digitalWrite ( NSRed, LOW ); //Turn on north/south red
  delay ( 3000 ); //Wait 3 seconds or 3000 milli seconds
  digitalWrite ( EWRed, HIGH ); //Turn off east/west red
  digitalWrite ( EWGreen, LOW ); //Turn on east/west green
  delay ( 3000 ); //Wait 3 seconds or 3000 milli seconds
  digitalWrite ( EWGreen, HIGH ); //Turn off east/west green
  digitalWrite ( EWYellow, LOW); //Turn on east/west yellow
  delay ( 2000 ); //Wait 2 seconds or 2000 milli seconds
  digitalWrite ( EWYellow, HIGH); //turn off east/west yellow for next pass
}

```

[![Here is the video:] (https://img.youtube.com/vi/gUKfZE8Fkjw/0.jpg)](https://www.youtube.com/watch?v=gUKfZE8Fkjw)




