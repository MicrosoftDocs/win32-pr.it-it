---
title: Attributo SAM-Account-Name
description: Nome di accesso utilizzato per supportare client e server che eseguono versioni precedenti del sistema operativo, ad esempio Windows NT 4.0, Windows 95, Windows 98 e LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo SAM-Account-Name
- Schema AD dell'attributo sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74aa558f63c2e1822f1435cdafd6290755b92b4d5e34c329d8472693f37185d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022229"
---
# <a name="sam-account-name-attribute"></a>Attributo SAM-Account-Name

Nome di accesso utilizzato per supportare client e server che eseguono versioni precedenti del sistema operativo, ad esempio Windows NT 4.0, Windows 95, Windows 98 e LAN Manager.

Questo attributo deve contenere al massimo 20 caratteri per supportare i client precedenti e non può contenere questi caratteri:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Voce | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | SAM-Account-Name                                                                         |
| Ldap-Display-Name | sAMAccountName                                                                           |
| Dimensione              | Massimo 20 caratteri.                                                                   |
| Aggiorna privilegio  | Amministratore di dominio                                                                     |
| Frequenza di aggiornamento  | Questo valore deve essere assegnato quando viene creato il record dell'account e non deve cambiare. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-Id-Guid    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                              |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



 

 





