---
title: Telephone-Number attributo
description: Numero di telefono primario.
ms.assetid: 6a7faad4-9d86-4821-9b00-67adbf1b05f2
ms.tgt_platform: multiple
keywords:
- Telephone-Number schema AD dell'attributo
- Schema AD dell'attributo telephoneNumber
topic_type:
- apiref
api_name:
- Telephone-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d86054b50ae511b3f519c1c289fb529eaa8a2e7279adb7b66cbfc2df32c3758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923121"
---
# <a name="telephone-number-attribute"></a>Telephone-Number attributo

Numero di telefono primario.



| Voce | Valore |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telephone-Number                                                                 |
| Ldap-Display-Name | telephoneNumber                                                                  |
| Dimensione              | \-                                                                               |
| Privilegio di aggiornamento  | Chiunque può aggiornare questo oggetto in base alla sicurezza dell'oggetto creato. |
| Frequenza di aggiornamento  | \-                                                                               |
| Attribute-Id      | 2.5.4.20                                                                         |
| System-Id-Guid    | bf967a49-0de6-11d0-a285-00aa003049e2                                             |
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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                 |
| Classi usate in        | [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classi usate in        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Camera**](c-room.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                               |
| MAPI-Id                | 0x3A08                                                                                                           |
| System-Only            | Falso                                                                                                            |
| Is-Single-Valued       | Vero                                                                                                             |
| Indicizzato             | Falso                                                                                                            |
| Nel catalogo globale      | Vero                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 64                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Classi usate in        | [**Organization**](c-organization.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classi usate in        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario posta elettronica**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Camera**](c-room.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classi usate in        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario posta elettronica**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Camera**](c-room.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classi usate in        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario posta elettronica**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Camera**](c-room.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Indicizzato             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Classi usate in        | [**documentSeries**](c-documentseries.md)<br/> [**Destinatario posta elettronica**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Ruolo dell'organizzazione**](c-organizationalrole.md)<br/> [**Unità organizzativa**](c-organizationalunit.md)<br/> [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Camera**](c-room.md)<br/> |



 

 





