---
title: Attributo Physical-Delivery-Office-Name
description: Contiene la posizione dell'ufficio nel luogo di lavoro dell'utente.
ms.assetid: a6be61bf-9a9a-4b97-bdf8-894c173efadd
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Physical-Delivery-Office-Name
- Schema AD dell'attributo physicalDeliveryOfficeName
topic_type:
- apiref
api_name:
- Physical-Delivery-Office-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a574c7214f18d9cef46a64885ca2855fdaf3227a9dece159458d5f1cb07d8b7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647771"
---
# <a name="physical-delivery-office-name-attribute"></a>Attributo Physical-Delivery-Office-Name

Contiene la posizione dell'ufficio nel luogo di lavoro dell'utente.



| Voce | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| CN                | Physical-Delivery-Office-Name                                                       |
| Ldap-Display-Name | physicalDeliveryOfficeName                                                          |
| Dimensione              | \-                                                                                  |
| Aggiorna privilegio  | Amministratore di dominio o proprietario dell'account.                                              |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e ogni volta che è necessario modificare la posizione dell'ufficio. |
| Attribute-Id      | 2.5.4.19                                                                            |
| System-Id-Guid    | bf9679f7-0de6-11d0-a285-00aa003049e2                                                |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                         |



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
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                            |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                            |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                               |
| MAPI-Id                | 0x3A19                                                                                                           |
| System-Only            | Falso                                                                                                            |
| A valore singolo       | Vero                                                                                                             |
| Indicizzato             | Vero                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| A valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| A valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| A valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





