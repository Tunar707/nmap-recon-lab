# Nmap Reconnaissance Report

## Executive Summary

A controlled vulnerability assessment was performed against the Metasploitable 2 virtual machine using Nmap. The assessment identified multiple legacy services, insecure protocols, outdated software versions, and intentionally vulnerable components designed for security training.

## Target Information

| Item | Value |
|------|------|
| Target | Metasploitable 2 |
| IP Address | 192.168.56.3 |
| Scanner | Kali Linux |
| Network | Host-only (192.168.56.0/24) |

## Findings Summary

| Port | Service | Severity | Observation |
|------|---------|----------|-------------|
| 21 | vsFTPd 2.3.4 | Critical | Known backdoored version detected |
| 23 | Telnet | High | Unencrypted remote administration |
| 80 | Apache HTTP | Medium | Legacy web server exposed |
| 139/445 | Samba | High | SMB file sharing available |
| 1524 | Root Bind Shell | Critical | Intentionally vulnerable remote shell |
| 3306 | MySQL | Medium | Legacy database service |
| 5432 | PostgreSQL | Medium | Legacy database service |
| 8180 | Apache Tomcat | Medium | Administrative web application |

## Risk Assessment

The target intentionally exposes numerous outdated and insecure services for educational purposes. Critical findings include a backdoored FTP service, an exposed bind shell, legacy remote administration protocols, and multiple outdated server applications.
