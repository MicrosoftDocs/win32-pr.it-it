---
title: Attributo SAM-account-type
description: Questo attributo contiene informazioni su ogni oggetto tipo di conto.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo SAM-account-type
- Schema AD dell'attributo sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965196"
---
# <a name="sam-account-type-attribute"></a>Attributo SAM-account-type

Questo attributo contiene informazioni su ogni oggetto tipo di conto. È possibile enumerare un elenco di tipi di conto oppure usare l'API informazioni di visualizzazione per creare un elenco. Poiché i computer, gli account utente normali e gli account attendibili possono anche essere enumerati come oggetti utente, i valori per questi account devono essere un intervallo contiguo.

I valori possibili per questo attributo sono i seguenti:

-   \_Oggetto di dominio SAM \_ 0x0
-   \_ \_ 0x10000000 oggetto gruppo Sam
-   \_ \_ \_ 0x10000001 oggetto gruppo non di sicurezza Sam \_
-   \_Oggetto alias Sam \_ 0x20000000
-   \_Oggetto alias Sam non di \_ sicurezza \_ \_ 0x20000001
-   \_ \_ 0x30000000 oggetto utente Sam
-   \_ \_ Account utente normale Sam \_ 0x30000000
-   \_Account del computer Sam \_ 0x30000001
-   \_Account attendibile Sam \_ 0x30000002
-   \_ \_ 0x40000000 gruppo Basic App Sam \_
-   \_ \_ 0x40000001 gruppo di query app Sam \_
-   \_Tipo di account SAM \_ \_ Max 0x7FFFFFFF



| Voce | Valore |
|-------------------|-----------------------------------------------------------------|
| CN                | Tipo di account SAM                                                |
| LDAP-Display-Name | sAMAccountType                                                  |
| Dimensione              | \-                                                              |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.                                |
| Frequenza di aggiornamento  | Questa impostazione viene impostata dal sistema operativo quando viene creato l'oggetto. |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-ID-GUID    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
| Sintassi            | [**Enumerazione**](s-enumeration.md)                            |



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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



 

 





