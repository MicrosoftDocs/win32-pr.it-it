---
title: 'Funzione Texture2D:: GatherRed (S, float, int2, int2, int2, int2)'
description: "Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Funzione Texture2D:: GatherRed (S, float, int2, int2, int2, int2)"
ms.assetid: 85C321CB-B77C-430B-921D-D56E5597B24A
keywords:
- Funzione GatherRed HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b17e192388b6fc439d31cfe35eca99168da1c3f5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234621"
---
# <a name="texture2dgatherredsfloatint2int2int2int2-function"></a>Funzione Texture2D:: GatherRed (S, float, int2, int2, int2, int2)

Restituisce i componenti rossi dei quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherRed(
  in SamplerState S,
  in float        Location,
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

[Metodi GatherRed](texture2d-gatherred.md)
</dt> </dl>

 

 




