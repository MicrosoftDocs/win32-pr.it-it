---
title: Attributo SAM-account-name
description: Nome di accesso utilizzato per supportare client e server che eseguono versioni precedenti del sistema operativo, ad esempio Windows NT 4,0, Windows 95, Windows 98 e LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- Attributo SAM-account-name-schema AD
- Schema AD dell'attributo sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875541"
---
# <a name="sam-account-name-attribute"></a>Attributo SAM-account-name

Nome di accesso utilizzato per supportare client e server che eseguono versioni precedenti del sistema operativo, ad esempio Windows NT 4,0, Windows 95, Windows 98 e LAN Manager.

Questo attributo deve essere composto da un massimo di 20 caratteri per supportare i client precedenti e non può contenere i caratteri seguenti:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Voce | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | Nome account SAM                                                                         |
| LDAP-Display-Name | sAMAccountName                                                                           |
| Dimensione              | almeno 20 caratteri.                                                                   |
| Privilegio aggiornamento  | Amministratore di dominio                                                                     |
| Frequenza di aggiornamento  | Questo valore deve essere assegnato quando il record dell'account viene creato e non deve essere modificato. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-ID-GUID    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
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
| È a valore singolo       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| È a valore singolo       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



 

 





