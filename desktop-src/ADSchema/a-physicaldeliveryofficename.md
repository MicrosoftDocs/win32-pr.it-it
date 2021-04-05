---
title: Physical-Delivery-Office-Name (attributo)
description: Contiene la posizione dell'ufficio nella sede di lavoro dell'utente.
ms.assetid: a6be61bf-9a9a-4b97-bdf8-894c173efadd
ms.tgt_platform: multiple
keywords:
- Physical-Delivery-Office-Name attributo AD schema
- Schema AD dell'attributo physicalDeliveryOfficeName
topic_type:
- apiref
api_name:
- Physical-Delivery-Office-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6633ff902ba50cfce12aca54cc092ca4760e665c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965084"
---
# <a name="physical-delivery-office-name-attribute"></a>Physical-Delivery-Office-Name (attributo)

Contiene la posizione dell'ufficio nella sede di lavoro dell'utente.



| Voce | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| CN                | Physical-Delivery-Office-Name                                                       |
| LDAP-Display-Name | physicalDeliveryOfficeName                                                          |
| Dimensione              | \-                                                                                  |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.                                              |
| Frequenza di aggiornamento  | Quando il record dell'utente viene creato e ogni volta che è necessario modificare la posizione dell'ufficio. |
| Attribute-Id      | 2.5.4.19                                                                            |
| System-ID-GUID    | bf9679f7-0de6-11d0-a285-00aa003049e2                                                |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                         |



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
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                            |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                            |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                           |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                               |
| MAPI-Id                | 0x3A19                                                                                                           |
| System-Only            | Falso                                                                                                            |
| È a valore singolo       | Vero                                                                                                             |
| Indicizzato             | Vero                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Classi utilizzate in        | [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziale**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





