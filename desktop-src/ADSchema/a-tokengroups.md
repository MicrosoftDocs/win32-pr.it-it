---
title: Token-Groups attributo
description: Attributo calcolato che contiene l'elenco di SID a causa di un'operazione di espansione transitiva dell'appartenenza a un gruppo in un determinato utente o computer. Non è possibile recuperare i gruppi di token se non è presente alcun catalogo globale per recuperare le appartenenze inversa transitive.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Token-Groups schema AD dell'attributo
- Schema AD dell'attributo tokenGroups
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8971f9ba5baead73b7704760dcc86430f5ce1a318ac6bcbd9dfaf4125a21af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022069"
---
# <a name="token-groups-attribute"></a>Token-Groups attributo

Attributo calcolato che contiene l'elenco di SID a causa di un'operazione di espansione transitiva dell'appartenenza a un gruppo in un determinato utente o computer. Non è possibile recuperare i gruppi di token se non è presente alcun catalogo globale per recuperare le appartenenze inversa transitive.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Token-Groups                         |
| Ldap-Display-Name | tokenGroups                          |
| Dimensione              | \-                                   |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.     |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1301              |
| System-Id-Guid    | b7c69e6d-2cc7-11d2-854e-00a0c983f608 |
| Sintassi            | [**String(Sid)**](s-string-sid.md)  |



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
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Falso                                                        |
| Indicizzato             | Falso                                                        |
| Nel catalogo globale      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Falso                                                        |
| Indicizzato             | Falso                                                        |
| Nel catalogo globale      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Falso                                                        |
| Indicizzato             | Falso                                                        |
| Nel catalogo globale      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Falso                                                        |
| Indicizzato             | Falso                                                        |
| Nel catalogo globale      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Falso                                                        |
| Indicizzato             | Falso                                                        |
| Nel catalogo globale      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Falso                                                        |
| Indicizzato             | Falso                                                        |
| Nel catalogo globale      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------------------|
| ID collegamento                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Is-Single-Valued       | Falso                                                        |
| Indicizzato             | Falso                                                        |
| Nel catalogo globale      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



 

 





