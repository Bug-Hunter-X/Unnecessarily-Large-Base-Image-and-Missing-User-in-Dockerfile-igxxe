# Unnecessarily Large Base Image and Missing User in Dockerfile

This repository demonstrates a common mistake in Dockerfiles: using a large base image and omitting a dedicated user.

## Bug

The original `Dockerfile` uses `ubuntu:latest`, a very large image.  It also doesn't create a dedicated user, increasing the security risk.  This results in larger image sizes and slower build times.

## Solution

The `Dockerfile_fixed` demonstrates the improved version. It uses a smaller base image, `python:3.9-slim-buster`, optimized for Python applications and includes a dedicated user for enhanced security.