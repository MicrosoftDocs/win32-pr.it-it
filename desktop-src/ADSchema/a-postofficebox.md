---
title: Attributo Post-Office-Box
description: Numero della casella Post Office per questo oggetto.
ms.assetid: e782271a-2f79-42af-9c62-5723917a6f47
ms.tgt_platform: multiple
keywords:
- Schema di AD per l'attributo Post-Office-Box
- Schema AD dell'attributo postOfficeBox
topic_type:
- apiref
api_name:
- Post-Office-Box
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc8edd327a8b7577e7a8256a8e2f082aad13c8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965348"
---
# <a name="post-office-box-attribute"></a>Attributo Post-Office-Box

Numero della casella Post Office per questo oggetto.



| Voce | Valore |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Casella Post-Office                                                             |
| LDAP-Display-Name | postOfficeBox                                                               |
| Dimensione              | \-                                                                          |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.                                      |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e ogni volta che l'indirizzo deve essere modificato. |
| Attribute-Id      | 2.5.4.18                                                                    |
| System-ID-GUID    | bf9679fb-0de6-11d0-a285-00aa003049e2                                        |
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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                           |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                               |
| MAPI-Id                | 0x3A2B                                                                                                           |
| System-Only            | Falso                                                                                                            |
| È a valore singolo       | Falso                                                                                                            |
| Indicizzato             | Falso                                                                                                            |
| Nel catalogo globale      | Falso                                                                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 40                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





