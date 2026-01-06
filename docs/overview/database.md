# Database Architecture

## Overview

This document describes the database architecture used by DekaLLM and the changes made to improve stability.

---

## Background

During the initial deployment of DekaLLM, the database experienced stability issues.  
The database frequently restarted or reverted unexpectedly, which affected system reliability.

Following an internal incident and CAB process, a database migration was performed to address these issues.

---

## Database Architecture Changes

![DekaLLM Database Before and After](Topology_-_DekaLLM_DB.png)

### Before

- Single PostgreSQL instance
- Limited CPU and memory resources
- Database instability during runtime

### After

- Database migrated to a database operator
- PostgreSQL runs as multiple instances
- Currently deployed with 3 database instances
- Improved stability compared to the initial deployment
