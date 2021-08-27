---
description: Rappresenta un istogramma di una trama.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixEngineHistogram
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e6235287d2d87bf6fe1bd79c13813e6bb8500bc3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622167"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>Struttura PixEngineHistogram

Rappresenta un istogramma di una trama.

## <a name="syntax"></a>Sintassi


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Members

**horizontalMin**  
Valori minimi per ogni componente X, Y, Z e W nell'asse orizzontale (dominio) dell'istogramma.

**horizontalMax**  
Valori massimi per ogni componente X, Y, Z e W nell'asse orizzontale (dominio) dell'istogramma.

**verticalMin**  
Valori minimi per ogni componente X, Y, Z e W nell'asse verticale (intervallo) dell'istogramma.

**verticalMax**  
Valori massimi per ogni componente X, Y, Z e W nell'asse verticale (intervallo) dell'istogramma.

**Datalength**  
Numero di campioni considerati nell'istogramma.

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



