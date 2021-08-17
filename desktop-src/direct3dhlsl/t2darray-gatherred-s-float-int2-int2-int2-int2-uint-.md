---
title: Funzione Texture2DArray::GatherRed(S,float,int2,int2,int2,int2,uint)
description: Restituisce i componenti rossi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, insieme allo stato del mapping delle sezioni. | Funzione Texture2DArray::GatherRed(S,float,int2,int2,int2,int2,uint)
ms.assetid: 9DD399A4-E6ED-499B-ACA3-28028C0AB271
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
ms.openlocfilehash: a9cfaac94e04eea0a93e5cf3570f3a5605d171cd3613f075925eecc8713a53d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788449"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2uint-function"></a>Funzione Texture2DArray::GatherRed(S,float,int2,int2,int2,int2,uint)

Restituisce i componenti rossi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, insieme allo stato del mapping delle sezioni.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Tipo: **SamplerState**

Indice del campionatore in base zero.

</dd> <dt>

*Località* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Coordinate di esempio (u,v).

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

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE** se tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati prelevati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **TemplateType**

Valore a quattro componenti il cui tipo è uguale al tipo di modello.

## <a name="remarks"></a>Commenti

I campioni di trama possono essere usati per l'interpolazione bilineare.

Questa funzione è supportata per i tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi GatherRed](texture2darray-gatherred.md)
</dt> </dl>

 

 
