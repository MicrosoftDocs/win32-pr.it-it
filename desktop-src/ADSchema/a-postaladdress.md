---
title: Postal-Address attributo
description: Indirizzo postale per l'oggetto.
ms.assetid: 85e96b88-8e58-4916-a333-59e3d4ed8025
ms.tgt_platform: multiple
keywords:
- Postal-Address schema AD dell'attributo
- Attributo postalAddress - Schema AD
topic_type:
- apiref
api_name:
- Postal-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfc8aa9b3dbdd1a91ed8a55f55a295c10353f88e6e7e01a852481ddb68163b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118682394"
---
# <a name="postal-address-attribute"></a>Postal-Address attributo

Indirizzo postale per l'oggetto.



| Voce | Valore |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Postal-Address                                                              |
| Ldap-Display-Name | postalAddress                                                               |
| Dimensione              | \-                                                                          |
| Aggiorna privilegio  | Amministratore di dominio o proprietario dell'account.                                      |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e ogni volta che è necessario modificare l'indirizzo. |
| Attribute-Id      | 2.5.4.16                                                                    |
| System-Id-Guid    | bf9679fc-0de6-11d0-a285-00aa003049e2                                        |
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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| A valore singolo       | Falso                                                                                                                                                                                                                                                                                                           |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                           |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                            |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| A valore singolo       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                               |
| MAPI-Id                | 0x810C                                                                                                           |
| System-Only            | Falso                                                                                                            |
| Is-Single-Valued       | Falso                                                                                                            |
| Indicizzato             | Falso                                                                                                            |
| Nel catalogo globale      | Falso                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 4096                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





