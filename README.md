# CargoSync-Demo

AI-Powered Shared Delivery & Route Optimization Platform

CargoSync AI is a premium logistics coordination platform prototype demonstrating how AI can coordinate deliveries across multiple businesses, reduce empty trips, improve vehicle utilization, optimize routes, and measure operational impact.

This repository contains the demo-first frontend prototype. It is intentionally designed to run independently of a production backend so the complete presentation flow remains reliable and deterministic.

Current Status

🟢 Frontend Demo: Complete

Area

Status

React + Vite

✅ Complete

Premium dark SaaS UI

✅ Complete

Design token system

✅ Complete

Application shell

✅ Complete

Reusable UI components

✅ Complete

Business dashboard

✅ Complete

Interactive order creation

✅ Complete

Admin operations dashboard

✅ Complete

Optimization queue

✅ Complete

AI optimization simulation

✅ Complete

Optimization results

✅ Complete

Animated route visualization

✅ Complete

Leaflet map

✅ Complete

Analytics / impact dashboard

✅ Complete

KPI count-up animations

✅ Complete

Page transitions

✅ Complete

Toast notifications

✅ Complete

Demo-data synchronization

✅ Complete

Responsive UI audit

✅ Complete

Backend integration

⏳ Future

Authentication / authorization

⏳ Future

Production database

⏳ Future

Real AI optimization

⏳ Future

Real-time GPS tracking

⏳ Future

Production deployment

⏳ Future

Important: This is a prototype/demo implementation. The main demo flow does not currently depend on a production backend, database, authentication provider, real GPS devices, or live optimization service.

Product Vision

CargoSync AI addresses a logistics problem in which multiple businesses can have deliveries traveling through nearby locations while vehicles return partially empty or completely empty.

The platform is designed around:

Shared delivery coordination

Order clustering

AI-assisted route optimization

Driver and vehicle assignment

Route visualization

Operational analytics

Fuel and distance reduction

CO₂ reduction measurement

Core workflow

Business Orders
      ↓
Order Clustering
      ↓
AI Route Optimization
      ↓
Driver / Vehicle Assignment
      ↓
Optimized Delivery Route
      ↓
Operational Impact
      ↓
Analytics & Insights

Demo-First Philosophy

The current implementation prioritizes:

Visual quality

Complete user flow

Demonstration reliability

Deterministic results

Clear communication of the AI concept

Reusable architecture

Easy replacement of simulated services with production services

The demo intentionally avoids infrastructure dependencies so the presentation remains repeatable.

Technology Stack

Frontend

React 19

Vite

JavaScript / JSX

React Router

Tailwind CSS v4

Lucide React

Recharts

Leaflet

React Leaflet

Axios

Backend Preparation

A FastAPI backend skeleton is already present for future integration.

Prepared dependencies include:

FastAPI

Uvicorn

python-dotenv

Supabase client

scikit-learn

Google OR-Tools

These are future integration foundations and are not required by the current frontend demo flow.

Repository Structure

cargo-sync-ai/
├── frontend/
│   ├── public/
│   └── src/
│       ├── assets/
│       ├── components/
│       │   ├── analytics/
│       │   ├── common/
│       │   ├── layout/
│       │   ├── map/
│       │   ├── orders/
│       │   └── ui/
│       ├── constants/
│       ├── context/
│       ├── features/
│       │   ├── analytics/
│       │   ├── map/
│       │   ├── optimization/
│       │   └── orders/
│       ├── hooks/
│       ├── layouts/
│       ├── lib/
│       ├── pages/
│       ├── services/
│       ├── styles/
│       ├── theme/
│       ├── types/
│       ├── App.jsx
│       ├── main.jsx
│       └── router.jsx
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
├── backend/
│   ├── api/
│   ├── database/
│   ├── models/
│   ├── optimization/
│   ├── schemas/
│   ├── services/
│   ├── utils/
│   ├── config.py
│   ├── main.py
│   └── requirements.txt
├── docs/
│   ├── PROJECT_RULES.md
│   ├── PROJECT_CONTEXT.md
│   ├── ROADMAP.md
│   ├── DEVELOPMENT_LOG.md
│   ├── MASTER_PROMPT.md
│   ├── DESIGN_SYSTEM.md
│   └── UI_SCREEN_SPECIFICATIONS.md
└── README.md

Application Architecture

React Router
     │
     ▼
Application Shell
Navbar + Sidebar
     │
     ├───────────────┬───────────────┐
     ▼               ▼               ▼
Business          Admin          Analytics
Dashboard         Dashboard       Dashboard
     │               │               │
     ▼               ▼               ▼
Orders          Optimization       Impact
Feature           Feature          Feature
     │               │               │
     └───────────────┼───────────────┘
                     ▼
              Reusable UI Layer
                     │
       Button / Card / Table / Badge /
       StatCard / Input / Select / Toast

Feature-specific functionality is isolated under src/features/, while generic primitives live under src/components/ui/.

This separation is intentional so future APIs and backend services can replace simulated data without requiring a complete UI rewrite.

Completed Features

1. Application Shell

Persistent sidebar

Collapsible navigation

Navbar

Page title context

Responsive content container

Nested React Router layouts

Active navigation states

Sidebar:

Expanded: 260px
Collapsed: 80px

2. Premium Dark Design System

The interface uses a professional dark SaaS visual system:

Deep navy foundation

Layered surfaces

Subtle borders

Controlled blue/violet gradients

High-contrast typography

Semantic status colors

Consistent spacing

Consistent radii

Soft shadows

Restrained glow effects

The design goal is an enterprise AI logistics product, not a generic dashboard template.

3. Reusable UI Component Library

Core

Button

Card

Input

Badge

Enterprise

Table

TableHeader

TableRow

TableCell

TablePagination

StatCard

StatCardTrend

SearchBox

Select

Textarea

Toast

Components use centralized design tokens wherever possible.

Business Dashboard

The Business Dashboard provides the operational view for businesses.

Includes

Active Orders KPI

Completed Today KPI

Distance Saved KPI

CO₂ Saved KPI

Quick Actions

Recent Orders

AI Optimization Status

Recent Activity

Create Order flow

Interactive Order Management

Orders currently use local React state.

Create Order

Users can enter:

Pickup

Delivery

Weight

Priority

Notes

Validation

The form validates:

Required pickup

Required delivery

Positive weight

Priority

Maximum note length

Dynamic behavior

Creating an order updates:

Recent Orders

KPI values

Recent Activity

Toast notification

No database is required for the current demo.

Admin Operations Center

The Admin Dashboard represents the logistics operations view.

Includes

Optimization KPIs

Optimization Queue

Driver Pool

AI Engine Status

Recent Optimizations

Optimization actions

Demo entities use synchronized identifiers such as:

CLS-408
CLS-409
CLS-410

AI Optimization Simulation

The optimization process is currently simulated on the frontend.

The presentation communicates a realistic optimization pipeline:

Scanning Orders
        ↓
Validating Delivery Constraints
        ↓
Applying DBSCAN Clustering
        ↓
Building Delivery Clusters
        ↓
Optimizing Route Trajectories
        ↓
Assigning Vehicles
        ↓
Generating Optimized Routes

The simulator provides:

Progress indicator

Current operation

ETA

Completed steps

Active step

Upcoming steps

Completion state

Results summary

This is a simulation of the future optimization engine, not a claim that DBSCAN/OR-Tools are currently executing in the frontend.

Optimization Results

The results experience communicates:

Distance saved

Fuel saved

CO₂ saved

Shared deliveries

Vehicle utilization

Before/after metrics

Assigned driver

Route sequence

AI-generated insights

The purpose is to clearly answer:

Why is the optimized route better?

Animated Route Visualization

The map is one of the primary demonstration features.

Technology

Leaflet

React Leaflet

Dark map tiles

Demonstration

A simulated delivery vehicle travels through the optimized route.

The map includes:

Warehouse

Pickup/delivery stops

Driver

Original route

Optimized route

Live timeline

Live savings statistics

Controls

Play

Pause

Replay

Animation

The truck uses requestAnimationFrame for smooth interpolation.

A completion state summarizes the final operational savings.

Analytics / Impact Dashboard

The Analytics Dashboard demonstrates measurable impact.

KPIs

Total Deliveries

Distance Saved

Fuel Saved

CO₂ Reduction

Vehicle Utilization

Shared Deliveries

Charts

Built with Recharts:

Distance trend

Fuel savings

Delivery breakdown

Vehicle utilization

Additional features

Driver performance table

AI insights

Export Report interaction

Interactive chart tooltips

The export workflow is currently simulated.

UX & Presentation Features

The prototype includes:

KPI Count-Up

Important numbers animate from zero to their target values.

Page Transitions

Subtle fade/slide transitions improve navigation continuity.

Toast Notifications

Operations such as order creation and report export provide immediate feedback.

AI Processing Animation

The optimization simulation communicates the processing stages visually.

Responsive Design

The UI has been checked against:

1920 × 1080
1600 × 900
1366 × 768
1280 × 720

Demo Data Strategy

The prototype uses deterministic demo data.

The same entities are synchronized across the application.

Demo Drivers

Rajesh Kumar

Amit Singh

Suresh Patil

Vikram Das

Demo Clusters

CLS-408

CLS-409

CLS-410

The same drivers, cluster IDs, route results, and savings narrative are reused across:

Business Dashboard

Admin Dashboard

Optimization Simulation

Optimization Results

Map

Analytics

This prevents contradictory information during demonstrations.

What Is Currently Simulated?

Capability

Current Implementation

Authentication

Skipped for demo

User identity

Demo context

Order persistence

Local React state

Database

Not required by demo

Order clustering

Simulated

DBSCAN

Demonstration narrative

Route optimization

Simulated

OR-Tools

Future-ready dependency

Driver assignment

Simulated

GPS tracking

Simulated animation

Route progress

Frontend animation

Analytics

Deterministic demo data

AI insights

Predefined demo insights

Report export

Simulated

Notifications

Frontend toast

Future-Ready Features

The architecture is intentionally prepared for a production version.

1. FastAPI Backend

Future flow:

React
  ↓
Axios Service Layer
  ↓
FastAPI
  ↓
Business Services

Potential API groups:

/orders
/drivers
/vehicles
/optimization
/routes
/analytics

2. Real AI Optimization

Future pipeline:

Orders
  ↓
Validation
  ↓
DBSCAN Spatial Clustering
  ↓
Constraint Processing
  ↓
OR-Tools Optimization
  ↓
Vehicle Assignment
  ↓
Route Generation
  ↓
Savings Calculation

Potential constraints:

Vehicle capacity

Delivery time windows

Driver availability

Priority

Distance

Route duration

Pickup/delivery relationships

3. DBSCAN Clustering

The frontend already represents the clustering concept.

Future backend implementation can use scikit-learn to cluster geographically compatible orders.

Potential inputs:

latitude
longitude
delivery radius
time window
priority
vehicle constraints

4. OR-Tools

The backend is prepared for Google OR-Tools.

Future use cases:

Vehicle Routing Problem

Capacitated VRP

Time-window routing

Multi-stop optimization

Vehicle assignment

Distance minimization

The frontend should receive the result rather than implement the optimization algorithm itself.

5. Real-Time GPS

Current:

useRouteAnimation()
       ↓
Simulated coordinates

Future:

Driver GPS
    ↓
GPS Gateway
    ↓
WebSocket
    ↓
FastAPI
    ↓
Frontend
    ↓
Live Map

The existing map UI is therefore a strong starting point for a real fleet-tracking experience.

6. Production Database

Supabase is already prepared in the backend dependencies.

Potential production entities:

users
businesses
drivers
vehicles
orders
order_items
delivery_clusters
optimization_runs
routes
route_stops
gps_locations
analytics_events
notifications

7. Authentication & RBAC

Authentication is intentionally skipped in the demo.

A production version can support:

Business User
Driver
Operations Admin
Super Admin

Potential permissions:

Role

Orders

Routes

Drivers

Analytics

Optimization

Business

✅

View

View

✅

Request

Driver

Assigned

Own

Own

Limited

—

Admin

✅

✅

✅

✅

✅

Super Admin

✅

✅

✅

✅

✅

8. Multi-Tenant Architecture

The core concept naturally supports multiple businesses.

CargoSync Platform
│
├── Business A
│   ├── Orders
│   ├── Drivers
│   └── Routes
│
├── Business B
│   ├── Orders
│   ├── Drivers
│   └── Routes
│
└── Shared Optimization Layer

Production implementation would require strong tenant isolation and server-side authorization.

9. Driver Application

A future driver application can provide:

Assigned route

Next stop

ETA

Delivery status

Navigation

Available capacity

Pickup confirmation

Delivery confirmation

GPS sharing

Route completion

Workflow:

Driver Login
     ↓
Assigned Route
     ↓
Start Route
     ↓
Navigate
     ↓
Pickup
     ↓
Delivery
     ↓
Next Stop
     ↓
Complete Route

10. Notifications

Future notification infrastructure can support:

New order assignment

Route changes

Driver arrival

Delivery delay

Optimization completion

Capacity warnings

Route exceptions

Possible channels:

In-app

Email

Push

SMS

11. Production Analytics

Future analytics can consume real operational events.

Operational

Deliveries completed

Average delivery time

Route distance

Vehicle utilization

Driver utilization

Financial

Fuel cost saved

Cost per delivery

Cost per kilometer

Route cost

Environmental

CO₂ avoided

Fuel reduction

Empty kilometers reduced

Optimization

Orders clustered

Routes optimized

Average optimization time

Optimization success rate

12. Reporting

Current export is a demo interaction.

Future reporting can support:

PDF

CSV

Excel

Scheduled reports

Email delivery

Possible reports:

Daily Operations Report
Weekly Optimization Report
Monthly Sustainability Report
Driver Performance Report
Business Savings Report

Production Architecture Direction

                 Load Balancer
                      │
              ┌───────▼───────┐
              │    Frontend   │
              └───────┬───────┘
                      │
                 API Gateway
                      │
              ┌───────▼───────┐
              │    FastAPI    │
              └───────┬───────┘
                      │
        ┌─────────────┼─────────────┐
        │             │             │
        ▼             ▼             ▼
    Database      Optimizer      Realtime
    /Supabase     Service        WebSocket
                      │
              ┌───────▼───────┐
              │ DBSCAN +      │
              │ OR-Tools      │
              └───────────────┘

Development History

Phase 0 — Bootstrap

React/Vite frontend

FastAPI skeleton

Dependencies

Documentation

Project structure

Phase 1 — Design Foundation

Theme tokens

Typography

Spacing

Global CSS

Application shell

Reusable UI components

Enterprise components

Phase 2 — Business Operations

Business Dashboard

Order management

Create Order drawer

Validation

Toast system

Phase 3 — AI Operations

Admin Dashboard

Optimization Queue

Driver Pool

AI Engine Status

Phase 4 — AI Demonstration

AI optimization simulator

Multi-step processing flow

Optimization results

Phase 5 — Route Visualization

Leaflet

Dark map

Animated truck

Route timeline

Playback controls

Completion state

Phase 6 — Analytics

Impact Dashboard

KPI visualization

Recharts

Driver performance

AI insights

Export interaction

Phase 7 — UX Polish

Count-up animations

Page transitions

Premium toast

Improved optimization narrative

Landing-page refinement

Phase 8 — Demo Readiness

Data synchronization

Navigation audit

Responsive audit

Performance verification

Frontend stability

Phase 8.1 — Premium Dark SaaS Redesign

Dark product foundation

Blue/violet accent system

Layered cards

Refined navigation

Premium landing page

Dark map

Dashboard restyling

AI simulation restyling

Analytics restyling

Current visual refinement direction

The next UI refinement is focused on:

Stronger information hierarchy

Better card proportions

More consistent spacing

Restrained gradients

Professional enterprise styling

Reduced visual clutter

Commercial SaaS appearance

Running the Project

Frontend

From the repository root:

cd cargo-sync-ai/frontend
npm install
npm run dev

Then open the URL printed by Vite, normally:

http://localhost:5173

If Vite selects another port, use the displayed port.

Backend Skeleton

The backend is not required for the main demo.

cd cargo-sync-ai/backend
pip install -r requirements.txt
python -m uvicorn main:app --reload

Health endpoint:

GET /

Expected:

{
  "status": "running"
}

Recommended Demo Flow

Landing Page
      ↓
Business Dashboard
      ↓
Create Order
      ↓
Order Appears
      ↓
Admin Dashboard
      ↓
Optimization Queue
      ↓
Click Optimize
      ↓
AI Optimization Simulation
      ↓
Optimization Complete
      ↓
View Optimized Route
      ↓
Animated Map
      ↓
Route Completion
      ↓
Analytics Dashboard
      ↓
Business Impact

The narrative is:

PROBLEM
  ↓
ORDERS
  ↓
COORDINATION
  ↓
AI OPTIMIZATION
  ↓
ROUTE
  ↓
SAVINGS
  ↓
MEASURABLE IMPACT

Demo Reliability

The current demo is deliberately decoupled from production infrastructure.

Advantages:

No authentication dependency

No database dependency

No AI server dependency

No GPS device dependency

No backend dependency for the main presentation

Deterministic demo data

Repeatable optimization flow

Repeatable map animation

Repeatable analytics

This makes the prototype reliable for demonstrations.

Current Limitations

The prototype is not yet a production logistics system.

Major limitations:

No real user authentication

No persistent production database

Orders currently use local demo state

AI optimization is simulated

Driver GPS is simulated

Route data is deterministic

Analytics use demo data

Export is simulated

No production notification infrastructure

No multi-tenant authorization

No production monitoring

No real external routing/traffic engine

These are intentional prototype boundaries.

Recommended Production Roadmap

P1  Backend API Foundation
        ↓
P2  Database + Data Models
        ↓
P3  Authentication + RBAC
        ↓
P4  Real Order Management API
        ↓
P5  DBSCAN Clustering
        ↓
P6  OR-Tools Route Optimization
        ↓
P7  Driver / Vehicle Management
        ↓
P8  Real-Time GPS + WebSockets
        ↓
P9  Production Analytics
        ↓
P10 Notifications + Reporting
        ↓
P11 Testing + Security
        ↓
P12 Cloud Deployment + Monitoring

Production Hardening Checklist

Authentication

Role-based access control

Database persistence

Server-side validation

Server-side authorization

Real optimization engine

Real GPS

WebSocket infrastructure

Error monitoring

Structured logging

Rate limiting

API security

Input sanitization

Automated tests

Integration tests

Load testing

Backup strategy

Environment-specific configuration

CI/CD

Production deployment

Monitoring and alerting

Final Status

🟢 COMPLETE — DEMO

CargoSync AI currently provides a polished, interactive frontend demonstrating:

Shared delivery

Order coordination

AI optimization concept

Driver assignment

Route optimization

Animated route execution

Savings measurement

Operational analytics

🟡 FUTURE-READY

The architecture is prepared for:

FastAPI

Supabase

DBSCAN

OR-Tools

Real GPS

WebSockets

Authentication

RBAC

Multi-tenancy

Production analytics

Reporting

Notifications

Cloud deployment

🔴 NOT PRODUCTION READY YET

The following require implementation before commercial deployment:

Authentication
Database Persistence
Real AI Optimization
Real GPS
Security
Multi-tenancy
Production APIs
Testing
Monitoring
Deployment

Product Story

CargoSync AI demonstrates the complete intended product journey:

Businesses create delivery orders → CargoSync identifies compatible delivery opportunities → AI clustering and route optimization coordinate them → a driver receives an efficient route → the route is executed → distance, fuel, cost, and CO₂ savings become measurable business outcomes.

The current frontend is intentionally separated from the future service layer, making it a strong foundation for production backend, optimization, real-time tracking, and multi-business functionality.
