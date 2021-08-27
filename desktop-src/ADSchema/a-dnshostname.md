---
title: Attributo DNS-Host-Name
description: Nome del computer registrato in DNS.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo DNS-Host-Name
- Schema AD dell'attributo dNSHostName
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241ea7144db7895e521c2844627d77b2f0ce54b5da518d180c87c6e9f834140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085961"
---
# <a name="dns-host-name-attribute"></a>Attributo DNS-Host-Name

Nome del computer registrato in DNS.



| Voce | Valore |
|-------------------|-----------------------------------------------------------------------------|
| CN                | DNS-Host-Name                                                               |
| Ldap-Display-Name | dNSHostName                                                                 |
| Dimensione              | Ogni segmento può contenere 63 caratteri. L'intera lunghezza può essere di 255 caratteri. |
| Aggiorna privilegio  | Amministratore di dominio                                                        |
| Frequenza di aggiornamento  | Quando il computer è denominato.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-Id-Guid    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi usate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi usate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------------|
| ID collegamento                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Is-Single-Valued       | Vero                                  |
| Indicizzato             | Falso                                 |
| Nel catalogo globale      | Vero                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classi usate in        | [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi usate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi usate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi usate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi usate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



 

 





