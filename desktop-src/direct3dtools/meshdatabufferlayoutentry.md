---
description: Rappresenta le informazioni su una singola voce nel layout del buffer di una mesh.
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
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747575"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Struttura MeshDataBufferLayoutEntry

Rappresenta le informazioni su una singola voce nel layout del buffer di una mesh.

## <a name="syntax"></a>Sintassi


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Members

**pName**  
Stringa COM contenente il nome della voce.

**numComponents**  
Numero di componenti omogenei (valori) che costituiscono questa voce.

**Posizione**  
true se la voce è una posizione; in caso contrario, false.

**format**  
Formato dati della voce (Register). Per ulteriori informazioni, vedere l' \_ enumerazione del formato Register.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



