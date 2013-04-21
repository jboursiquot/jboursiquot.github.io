---
layout: post
title: "MSSQL DB Restore Error: Media set has 2 families but only 1 are provided"
description:
category: 
tags: [mssql]
published: true
---

While deploying a Microsoft SQL Server 2008 R2 database, I came across this weird error: "This media set has 2 media families but only 1 are provided."

<img alt="MSSQL Database Export Destination" height="163" src="/assets/content-images/mssql-error-12-26-2011.png" width="611" class="post-image">

Searching the net didn't really provide an immediate solution but did hint at the fact that the backup device that was used for the database I'm trying to import specified a couple of locations and not just the 1 I was specifying during import.

After performing the backup once more, this time making sure to only have just one entry in the Destination of the backup window, things worked as expected when imported on the other server.

<img align="middle" alt="MSSQL Database Export Destination" height="188"
src="/assets/content-images/mssql-error-12-26-2011-1.png" width="509" class="post-image">

Hopefully this will save someone else some time.
