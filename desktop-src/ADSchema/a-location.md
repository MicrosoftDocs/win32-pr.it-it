---
title: Location (attributo)
description: Posizione dell'utente, ad esempio numero di ufficio.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Schema di AD dell'attributo location
- Schema di AD dell'attributo location
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a37f15e80d470c0662036745f285aea87e79391
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122586"
---
# <a name="location-attribute-ad-schema"></a>Attributo location (schema AD)

Posizione dell'utente, ad esempio numero di ufficio.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Location                                    |
| LDAP-Display-Name | posizione                                    |
| Dimensione              | \-                                          |
| Privilegio aggiornamento  | \-                                          |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-ID-GUID    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                            |
| È a valore singolo       | Vero                                                                                                                                                             |
| Indicizzato             | Vero                                                                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| Classi utilizzate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi utilizzate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------|
| ID collegamento                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| È a valore singolo       | Vero                                                                    |
| Indicizzato             | Vero                                                                    |
| Nel catalogo globale      | Vero                                                                    |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| Classi utilizzate in        | [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi utilizzate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi utilizzate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi utilizzate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi utilizzate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



 

 





