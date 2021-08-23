---
title: Attributo RID-Previous-Allocation-Pool
description: Contiene il pool di identificatori relativi (RID) da cui viene allocato un controller di dominio.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo RID-Previous-Allocation-Pool
- Schema AD dell'attributo rIDPreviousAllocationPool
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199d9fd0f91b94ed6625a8759f3a5acd76a892460c44e3315911350f0ff59f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837361"
---
# <a name="rid-previous-allocation-pool-attribute"></a>Attributo RID-Previous-Allocation-Pool

**L'attributo RID-Previous-Allocation-Pool** contiene il pool di identificatori relativi (RID) da cui viene allocato un controller di dominio. Questo attributo è un valore a otto byte che contiene una coppia di numeri interi a quattro byte che rappresentano i valori iniziale e finale del pool di RID. Il valore iniziale si trova nei quattro byte inferiori e il valore finale è nei quattro byte superiori.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | RID-Previous-Allocation-Pool         |
| Ldap-Display-Name | rIDPreviousAllocationPool            |
| Dimensione              | \-                                   |
| Privilegio di aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-Id-Guid    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
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
| System-Flags           | 0x00000011                             |
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
| System-Flags           | 0x00000011                             |
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
| System-Flags           | 0x00000011                             |
| Classi usate in        | [**SET RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



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
| System-Flags           | 0x00000011                             |
| Classi usate in        | [**SET RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



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
| System-Flags           | 0x00000011                             |
| Classi usate in        | [**SET RID**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



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
| System-Flags           | 0x00000011                             |
| Classi usate in        | [**SET RID**](c-ridset.md)<br/> |



 

 





