---
title: RID-Previous-allocation-attributo pool
description: Contiene il pool di identificatori relativi (RID) da cui viene allocato un controller di dominio.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-precedente-allocazione-schema AD attributo pool
- Schema AD dell'attributo rIDPreviousAllocationPool
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875166"
---
# <a name="rid-previous-allocation-pool-attribute"></a>RID-Previous-allocation-attributo pool

L'attributo **RID-Previous-allocation-pool** contiene il pool di identificatori relativi (RID) da cui viene allocato un controller di dominio. Questo attributo è un valore di otto byte che contiene una coppia di interi a quattro byte che rappresentano i valori iniziale e finale del pool di RID. Il valore iniziale è nei quattro byte inferiori e il valore finale è nei quattro byte superiori.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | RID-precedente-allocazione-pool         |
| LDAP-Display-Name | rIDPreviousAllocationPool            |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-ID-GUID    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
| Sintassi            | [**Interval**](s-interval.md)       |



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
| È a valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classi utilizzate in        | [**Set RID**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| È a valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classi utilizzate in        | [**Set RID**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| È a valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classi utilizzate in        | [**Set RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| È a valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classi utilizzate in        | [**Set RID**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| È a valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classi utilizzate in        | [**Set RID**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------|
| ID collegamento                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Vero                                   |
| È a valore singolo       | Vero                                   |
| Indicizzato             | Falso                                  |
| Nel catalogo globale      | Falso                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| Classi utilizzate in        | [**Set RID**](c-ridset.md)<br/> |



 

 





