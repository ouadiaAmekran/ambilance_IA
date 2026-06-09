# Smart Ambulance AI Dispatch System

## Overview

This project addresses a life-critical problem in emergency medical services: how to route ambulances optimally under real-time conditions to minimize response times and maximize survival outcomes. The system developed here combines deep learning with geospatial intelligence to build an AI-powered dispatch platform capable of making routing decisions faster and more accurately than traditional manual dispatch.

In emergency medicine, the time between an incident and the arrival of medical responders is one of the strongest predictors of patient outcomes. Shaving minutes off response times — especially in dense urban environments with complex traffic dynamics — has measurable impact on lives saved.

## What Was Built

The platform takes incoming emergency calls, processes their location data, and uses a deep learning model trained on historical incident data to predict optimal dispatch decisions: which ambulance unit to assign, which route to take, and how to account for real-time traffic and other active incidents. The geographic routing and visualization layer was built using Mapbox, enabling real-time map display of unit positions, incident locations, and recommended routes.

The ETL pipeline was responsible for ingesting and preprocessing the training data — historical dispatch records, geographic information, and traffic patterns — transforming it into feature-rich datasets suitable for model training. Flask served as the lightweight backend API framework, handling real-time requests from the frontend dispatch interface and coordinating with the model inference layer.

The deep learning model was trained to balance multiple competing objectives simultaneously: minimizing travel time, avoiding unit clustering, and ensuring coverage across the service area at all times.

## Why This Project Matters

Emergency dispatch optimization is a high-stakes, real-time machine learning problem. The system must operate under uncertainty — traffic changes, multiple simultaneous incidents, varying unit availability — and produce reliable recommendations in seconds. This pushes the design toward robust architectures that can handle streaming data and partial information gracefully.

The integration with a live geospatial visualization platform also reflects production-level thinking: a dispatch system that works in theory but is unusable in a control room environment has no real value. Building the Mapbox-powered interface ensured the system could actually be used by human dispatchers in a real operational context.

## Technologies Used

Python, Flask, Mapbox (geospatial visualization), Deep Learning, ETL pipelines.
