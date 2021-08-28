---
title: Attributo Surname
description: Questo attributo contiene la famiglia o il cognome di un utente.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Attributo surname Schema DI AD
- Schema AD dell'attributo sn
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655557c23475dbc2d7f2e92fb48f5f71a8e818954bff83f5a47bb2470a26ca20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836191"
---
# <a name="surname-attribute"></a>Attributo Surname

Questo attributo contiene la famiglia o il cognome di un utente.



| Voce | Valore |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Surname                                                                          |
| Ldap-Display-Name | sn                                                                               |
| Dimensione              | \-                                                                               |
| Privilegio di aggiornamento  | Chiunque può aggiornare questo oggetto in base alla sicurezza dell'oggetto creato. |
| Frequenza di aggiornamento  | \-                                                                               |
| Attribute-Id      | 2.5.4.4                                                                          |
| System-Id-Guid    | bf967a41-0de6-11d0-a285-00aa003049e2                                             |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|---------------------------------------|
| ID collegamento                | \-                                    |
| MAPI-Id                | 0x3A11                                |
| System-Only            | Falso                                 |
| Is-Single-Valued       | Vero                                  |
| Indicizzato             | Vero                                  |
| Nel catalogo globale      | Vero                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 64                                    |
| Search-Flags           | 0x00000005                            |
| System-Flags           | 0x00000010                            |
| Classi usate in        | [**Persona**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| Is-Single-Valued       | Vero                                                                                          |
| Indicizzato             | Vero                                                                                          |
| Nel catalogo globale      | Vero                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classi usate in        | [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| Is-Single-Valued       | Vero                                                                                          |
| Indicizzato             | Vero                                                                                          |
| Nel catalogo globale      | Vero                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classi usate in        | [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| A valore singolo       | Vero                                                                                          |
| Indicizzato             | Vero                                                                                          |
| Nel catalogo globale      | Vero                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classi usate in        | [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| A valore singolo       | Vero                                                                                          |
| Indicizzato             | Vero                                                                                          |
| Nel catalogo globale      | Vero                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classi usate in        | [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falso                                                                                         |
| A valore singolo       | Vero                                                                                          |
| Indicizzato             | Vero                                                                                          |
| Nel catalogo globale      | Vero                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Classi usate in        | [**Persona**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





