---
description: Rappresenta i campi di layout di input di un vertex buffer, uno per ogni campo nel vertex buffer.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura InputLayoutStruct
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f5ad2552fe3c0c4b2ebc9919b4bcbd0375d73109
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631389"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span id="vspixengine.inputlayoutstruct"></span>Struttura InputLayoutStruct

Rappresenta i campi di layout di input di un vertex buffer, uno per ogni campo nel vertex buffer.

## <a name="syntax"></a>Sintassi


```C++
} InputLayoutStruct;
```

## <a name="members"></a>Members

**SemanticName**  
Stringa COM contenente il nome della semantica associata.

**SemanticIndex**  
Indice della semantica associata.

**Formato**  
Formato del campo. Per altre informazioni, vedere l'enumerazione DXGI \_ FORMAT.

**InputSlot**  
Slot di input associato.

**AlignedByteOffset**  

**Classe InputSlotClass**  

**InstanceDataStepRate**  

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



