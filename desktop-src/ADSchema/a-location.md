---
title: Location (attributo)
description: Posizione dell'utente, ad esempio il numero di ufficio.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo location
- Schema AD dell'attributo location
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7e8080ffa24c9b2a147e6e3ec76f586a92fba3456aa1f80d2875c1292940232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705771"
---
# <a name="location-attribute-ad-schema"></a>Attributo Location (schema AD)

Posizione dell'utente, ad esempio il numero di ufficio.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Località                                    |
| Ldap-Display-Name | posizione                                    |
| Dimensione              | \-                                          |
| Privilegio di aggiornamento  | \-                                          |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-Id-Guid    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
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
| Is-Single-Valued       | Vero                                                                                                                                                             |
| Indicizzato             | Vero                                                                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| Classi usate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi usate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------|
| ID collegamento                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Is-Single-Valued       | Vero                                                                    |
| Indicizzato             | Vero                                                                    |
| Nel catalogo globale      | Vero                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| Classi usate in        | [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi usate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi usate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi usate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                                                                               |
| Indicizzato             | Vero                                                                                                                                                                                               |
| Nel catalogo globale      | Vero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classi usate in        | [**Computer**](c-computer.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Camera**](c-room.md)<br/> [**Sito**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



 

 





