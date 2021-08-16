---
title: Attributo State-Or-Province-Name
description: Nome dello stato o della provincia di un utente.
ms.assetid: 2096318e-29bf-4021-a422-371835f3a62b
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo State-Or-Province-Name
- Schema AD dell'attributo st
topic_type:
- apiref
api_name:
- State-Or-Province-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c818eb0a885d598edc10b5857aee23e336095c301d3b1059b25ba7b2f9fd986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959990"
---
# <a name="state-or-province-name-attribute"></a>Attributo State-Or-Province-Name

Nome dello stato o della provincia di un utente.



| Voce | Valore |
|-------------------|----------------------------------------------------------------------------------|
| CN                | State-or-Province-Name                                                           |
| Ldap-Display-Name | st                                                                               |
| Dimensione              | \-                                                                               |
| Aggiorna privilegio  | Chiunque può aggiornare questo oggetto in base alla sicurezza dell'oggetto creato. |
| Frequenza di aggiornamento  | \-                                                                               |
| Attribute-Id      | 2.5.4.8                                                                          |
| System-Id-Guid    | bf967a39-0de6-11d0-a285-00aa003049e2                                             |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| A valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classi usate in        | [**Località**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| A valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classi usate in        | [**Località**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona erta**](c-residentialperson.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                         |
| MAPI-Id                | 0x3A28                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 128                                                                                                                                                        |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| Classi usate in        | [**Località**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classi usate in        | [**Località**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classi usate in        | [**Località**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classi usate in        | [**Località**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                      |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                     |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| Classi usate in        | [**Località**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona residenziali**](c-residentialperson.md)<br/> |



 

 





