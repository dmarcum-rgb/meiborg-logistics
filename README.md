# Meiborg TMS

**AI-powered fleet management platform built for Meiborg operations.**

An agentic dispatcher that autonomously matches loads to trucks, ensures HOS compliance, and optimizes routes — tailored for the Meiborg trucking team.

---

## Overview

Meiborg TMS is an internal transportation management system that combines AI-driven dispatch automation with real-time fleet visibility. Built on top of a modern multi-tenant architecture, it gives Meiborg dispatchers and drivers a single platform to manage loads, routes, compliance, invoicing, and payroll.

## Key Features

- **AI Agentic Dispatcher** — Automatically matches available loads to the right trucks based on location, HOS status, and capacity
- - **HOS Compliance** — Real-time Hours of Service tracking to keep Meiborg drivers compliant
  - - **Route Optimization** — Intelligent routing to minimize fuel costs and delivery times
    - - **Real-Time GPS Tracking** — Live map view of all Meiborg trucks and loads
      - - **Load Management** — Full load lifecycle from creation to delivery confirmation
        - - **Driver Mobile App** — Android/iOS app for Meiborg drivers (built with .NET MAUI)
          - - **Invoicing & Payroll** — Automated invoice generation and driver pay calculation
            - - **Multi-Tenant Architecture** — Supports multiple Meiborg divisions or clients
              - - **Customer Portal** — External portal for Meiborg customers to track their shipments
               
                - ## Tech Stack
               
                - | Layer | Technology |
                - |---|---|
                - | Backend API | ASP.NET Core, C# |
                - | Frontend | Angular (TMS Portal, Admin Portal, Website, Customer Portal) |
                - | Mobile | .NET MAUI (Android/iOS) |
                - | AI Dispatch | Agentic AI with custom skills |
                - | Maps | Mapbox |
                - | Auth | ASP.NET Identity Server |
                - | Database | Entity Framework Core |
                - | Infrastructure | Docker, Kubernetes, .NET Aspire |
                - | Payments | Stripe |
               
                - ## Repository Structure
               
                - ```
                  src/
                    Aspire/          # .NET Aspire orchestration
                    Client/
                      Logistics.Angular/
                        projects/
                          tms-portal/        # Main dispatcher TMS web app
                          admin-portal/      # Meiborg admin dashboard
                          customer-portal/   # Customer-facing shipment tracking
                          website/           # Public marketing site
                      Logistics.DriverApp/   # Mobile driver app (.NET MAUI)
                    Core/            # Domain models and business logic
                    Infrastructure/  # Database, external services
                    Presentation/    # API controllers
                    Shared/          # Shared utilities and contracts
                  ```

                  ## Getting Started

                  ### Prerequisites

                  - .NET 9 SDK
                  - - Node.js / Bun
                    - - Docker
                      - - Angular CLI
                       
                        - ### Running Locally
                       
                        - ```bash
                          # Install frontend dependencies
                          bun install

                          # Start the backend via Aspire
                          dotnet run --project src/Aspire/Logistics.AppHost

                          # Start the Angular TMS portal
                          cd src/Client/Logistics.Angular
                          bun run start:tms
                          ```

                          ---

                          *Meiborg TMS is an internal platform maintained by the Meiborg technology team.*
