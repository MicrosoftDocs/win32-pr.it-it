---
title: Attributo SAM-Account-Type
description: Questo attributo contiene informazioni su ogni oggetto tipo di account.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo SAM-Account-Type
- Schema AD dell'attributo sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132532af58eafa4950f049fb08ff7a4235cb49ac2b1f62fc832e308e7ab6d31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423388"
---
# <a name="sam-account-type-attribute"></a>Attributo SAM-Account-Type

Questo attributo contiene informazioni su ogni oggetto tipo di account. È possibile enumerare un elenco di tipi di account oppure usare l'API Visualizza informazioni per creare un elenco. Poiché i computer, gli account utente normali e gli account attendibili possono essere enumerati come oggetti utente, i valori per questi account devono essere un intervallo contiguo.

I valori possibili per questo attributo sono i seguenti:

-   OGGETTI DI DOMINIO SAM \_ \_ 0x0
-   OGGETTO GRUPPO SAM \_ \_ 0x10000000
-   OGGETTO GRUPPO DI SICUREZZA \_ SAM NON \_ \_ \_ 0X10000001
-   OGGETTO ALIAS SAM \_ \_ 0x20000000
-   OGGETTO ALIAS \_ SAM NON DI SICUREZZA \_ \_ \_ 0x20000001
-   OGGETTI UTENTE SAM \_ \_ 0x30000000
-   ACCOUNT \_ UTENTE NORMALE SAM \_ \_ 0x30000000
-   ACCOUNT \_ COMPUTER \_ SAM 0x30000001
-   ACCOUNT \_ \_ ATTENDIBILITÀ SAM 0x30000002
-   GRUPPO \_ DI \_ BASE \_ DELL'APP SAM 0x40000000
-   GRUPPO \_ DI QUERY DI APP SAM \_ \_ 0x40000001
-   SAM \_ ACCOUNT TYPE MAX \_ \_ 0x7fffffff



| Voce | Valore |
|-------------------|-----------------------------------------------------------------|
| CN                | SAM-Account-Type                                                |
| Ldap-Display-Name | sAMAccountType                                                  |
| Dimensione              | \-                                                              |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.                                |
| Frequenza di aggiornamento  | Questa proprietà viene impostata dal sistema operativo quando viene creato l'oggetto . |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-Id-Guid    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
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
| Is-Single-Valued       | Vero                                                         |
| Indicizzato             | Vero                                                         |
| Nel catalogo globale      | Vero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
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
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



 

 





