---
title: Attributo DNS-host-name
description: Nome del computer registrato in DNS.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- DNS-host-name attributo AD schema
- Schema AD dell'attributo dNSHostName
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7580a58e5d3042633a9dd665354bc883b4fdb87c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519486"
---
# <a name="dns-host-name-attribute"></a>Attributo DNS-host-name

Nome del computer registrato in DNS.



| Voce | Valore |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Nome-host-DNS                                                               |
| LDAP-Display-Name | dNSHostName                                                                 |
| Dimensione              | Ogni segmento può essere costituito da 63 caratteri. La lunghezza intera può essere di 255 caratteri. |
| Privilegio aggiornamento  | Amministratore di dominio                                                        |
| Frequenza di aggiornamento  | Quando il computer è denominato.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-ID-GUID    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| È a valore singolo       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-registrazione-servizio**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| È a valore singolo       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-registrazione-servizio**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|---------------------------------------|
| ID collegamento                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| È a valore singolo       | Vero                                  |
| Indicizzato             | Falso                                 |
| Nel catalogo globale      | Vero                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classi utilizzate in        | [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| È a valore singolo       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-registrazione-servizio**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| È a valore singolo       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-registrazione-servizio**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| È a valore singolo       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-registrazione-servizio**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| È a valore singolo       | Vero                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Autorità di certificazione**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-registrazione-servizio**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



 

 





