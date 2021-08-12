---
description: Rappresenta informazioni su una singola voce nel layout del buffer di una mesh.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura MeshDataBufferLayoutEntry
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44cc67402c69b690ba9070fa51bf8d26f316faa7d10ac991226db2c05b6d6a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282275"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Struttura MeshDataBufferLayoutEntry

Rappresenta informazioni su una singola voce nel layout del buffer di una mesh.

## <a name="syntax"></a>Sintassi


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Members

**Pname**  
Stringa COM contenente il nome della voce.

**numComponents**  
Numero di componenti omogenei (valori) che costituiscono questa voce.

**isPosition**  
true se la voce è una posizione; in caso contrario, false.

**format**  
Formato dei dati della voce (registro). Per altre informazioni, vedere l'enumerazione REGISTER \_ FORMAT.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



