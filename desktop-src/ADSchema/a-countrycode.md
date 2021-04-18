---
title: Attributo Country-Code
description: Specifica il codice paese/area geografica per la lingua scelta dall'utente. Questo valore non viene utilizzato da Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Schema AD Country-Code attribute
- Schema AD dell'attributo countryCode
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303605"
---
# <a name="country-code-attribute"></a>Attributo Country-Code

Specifica il codice paese/area geografica per la lingua scelta dall'utente. Questo valore non viene utilizzato da Windows 2000.



| Voce | Valore |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| LDAP-Display-Name | countryCode                             |
| Dimensione              | 2 byte                                 |
| Privilegio aggiornamento  | Proprietario dell'account o amministratore di dominio   |
| Frequenza di aggiornamento  | Quando cambia il paese o l'area geografica dell'utente. |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| System-ID-GUID    | 5fd42471-1262-11d0-a060-00aa006c33ed    |
| Sintassi            | [**Enumerazione**](s-enumeration.md)    |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| È a valore singolo       | Vero                                                                                                                              |
| Indicizzato             | Falso                                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| È a valore singolo       | Vero                                                                                                                              |
| Indicizzato             | Falso                                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|----------------------------------------------------------------|
| ID collegamento                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| È a valore singolo       | Vero                                                           |
| Indicizzato             | Falso                                                          |
| Nel catalogo globale      | Falso                                                          |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| Classi utilizzate in        | [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| È a valore singolo       | Vero                                                                                                                              |
| Indicizzato             | Falso                                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| È a valore singolo       | Vero                                                                                                                              |
| Indicizzato             | Falso                                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| È a valore singolo       | Vero                                                                                                                              |
| Indicizzato             | Falso                                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| È a valore singolo       | Vero                                                                                                                              |
| Indicizzato             | Falso                                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



 

 





