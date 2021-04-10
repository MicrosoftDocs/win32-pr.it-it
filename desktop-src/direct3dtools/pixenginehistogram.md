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
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124683"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>Struttura PixEngineHistogram

Rappresenta un istogramma di una trama.

## <a name="syntax"></a>Sintassi


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Members

**horizontalMin**  
Valori minimi per ognuno dei componenti X, Y, Z e W nell'asse orizzontale (dominio) dell'istogramma.

**horizontalMax**  
Valori massimi per ognuno dei componenti X, Y, Z e W nell'asse orizzontale (dominio) dell'istogramma.

**verticalMin**  
Valori minimi per ognuno dei componenti X, Y, Z e W nell'asse verticale (intervallo) dell'istogramma.

**verticalMax**  
Valori massimi per ognuno dei componenti X, Y, Z e W nell'asse verticale (intervallo) dell'istogramma.

**dataLength**  
Numero di campioni considerati nell'istogramma.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



