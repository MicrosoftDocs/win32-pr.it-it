---
title: Funzione Texture2DArray::GatherCmpBlue(S,float,float,int2,int2,int2,int2,int2)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente blu e un valore di confronto. | Funzione Texture2DArray::GatherCmpBlue(S,float,float,int2,int2,int2,int2,int2)
ms.assetid: 1EAC38DC-51F5-41B8-926F-8D0626C37798
keywords:
- Funzione GatherCmpBlue HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9a3e86398fdda94a686a52bab04fb3313857d2172e536a3b8ca832234233d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788916"
---
# <a name="texture2darraygathercmpbluesfloatfloatint2int2int2int2-function"></a>Funzione Texture2DArray::GatherCmpBlue(S,float,float,int2,int2,int2,int2,int2)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il componente blu e un valore di confronto.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherCmpBlue(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Tipo: **SamplerState**

Indice del campionatore in base zero.

</dd> <dt>

*Posizione* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Coordinate di esempio (u,v).

</dd> <dt>

*CompareValue* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore da confrontare con ogni valore campionato.

</dd> <dt>

*Offset1* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Primo componente di offset applicato alle coordinate della trama prima del campionamento.

</dd> <dt>

*Offset2* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Secondo componente di offset applicato alle coordinate della trama prima del campionamento.

</dd> <dt>

*Offset3* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Terzo componente di offset applicato alle coordinate della trama prima del campionamento.

</dd> <dt>

*Offset4* \[ Pollici\]
</dt> <dd>

Tipo: **int2**

Quarto componente di offset applicato alle coordinate della trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **TemplateType**

Valore a quattro componenti il cui tipo è uguale al tipo di modello.

## <a name="remarks"></a>Commenti

Gli esempi di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherCmpBlue](texture2darray-gathercmpblue.md)
</dt> </dl>

 

 




