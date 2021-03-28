---
title: 'Funzione Texture2D:: GatherCmpRed (S, float, float, int2, int2, int2, int2)'
description: "Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto. | Funzione Texture2D:: GatherCmpRed (S, float, float, int2, int2, int2, int2)"
ms.assetid: B20A766E-0B4F-4FBA-A691-70ACE7BECF33
keywords:
- Funzione GatherCmpRed HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f84467c798337ac2cc81283637636900933c9e41
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969121"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2-function"></a>Funzione Texture2D:: GatherCmpRed (S, float, float, int2, int2, int2, int2)

Per quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto tra il relativo componente rosso e un valore di confronto.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherCmpRed(
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

*Posizione* \[ in\]
</dt> <dd>

Tipo: **float**

Coordinate di esempio (u, v).

</dd> <dt>

*CompareValue* \[ in\]
</dt> <dd>

Tipo: **float**

Valore da confrontare con ogni valore campionato.

</dd> <dt>

*Offset1* \[ in\]
</dt> <dd>

Tipo: **int2**

Primo componente di offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Offset2* \[ in\]
</dt> <dd>

Tipo: **int2**

Secondo componente di offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Offset3* \[ in\]
</dt> <dd>

Tipo: **int2**

Terzo componente di offset applicato alle coordinate di trama prima del campionamento.

</dd> <dt>

*Offset4* \[ in\]
</dt> <dd>

Tipo: **int2**

Quarto componente di offset applicato alle coordinate di trama prima del campionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **TemplateType**

Valore a quattro componenti il cui tipo corrisponde al tipo di modello.

## <a name="remarks"></a>Commenti

Gli esempi di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherCmpRed](texture2d-gathercmpred.md)
</dt> </dl>

 

 




