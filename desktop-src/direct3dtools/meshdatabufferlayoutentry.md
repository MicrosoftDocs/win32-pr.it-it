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
ms.openlocfilehash: 40360e73f480b4c12dcb24311c26fd9718093705
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625357"
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



