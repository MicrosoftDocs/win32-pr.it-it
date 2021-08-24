---
title: Attributo RID-Allocation-Pool
description: Pool che è stato preletturato per l'uso da parte del gestore RID quando è stato utilizzato RID-Previous-Allocation-Pool.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo RID-Allocation-Pool
- Schema AD dell'attributo rIDAllocationPool
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6ff101ca49e8d2ffafdb31f2d05cf1cb2371ee3336525ab31318925d349805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837381"
---
# <a name="rid-allocation-pool-attribute"></a>Attributo RID-Allocation-Pool

Pool che è stato preletturato per l'uso da parte del gestore RID quando è stato utilizzato RID-Previous-Allocation-Pool.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | RID-Allocation-Pool                  |
| Ldap-Display-Name | rIDAllocationPool                    |
| Dimensione              | 8 byte                              |
| Privilegio di aggiornamento  | Questo valore viene impostato dal sistema.     |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.371               |
| System-Id-Guid    | 66171889-8f3c-11d0-afda-00c04fd930c9 |
| Sintassi            | [**Intervallo**](s-interval.md)       |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| Is-Single-Valued       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classi usate in        | [**SET RID**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| Is-Single-Valued       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classi usate in        | [**SET RID**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| Is-Single-Valued       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classi usate in        | [**SET RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| A valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classi usate in        | [**SET DI RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| A valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classi usate in        | [**SET DI RID**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| A valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000010                             |
| Classi usate in        | [**SET DI RID**](c-ridset.md)<br/> |



 

 





