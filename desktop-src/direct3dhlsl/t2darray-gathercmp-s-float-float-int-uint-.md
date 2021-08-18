---
title: Funzione Texture2DArray::GatherCmp(S,float,float,int,uint)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto con un valore di confronto insieme allo stato del mapping dei riquadri. | Funzione Texture2DArray::GatherCmp(S,float,float,int,uint)
ms.assetid: E68619B2-6AB0-4C57-9604-7759FD987446
keywords:
- Funzione GatherCmp HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b99839c9151264b7eb392d50c61438e9a2796fb56692b7830131797070c49c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723856"
---
# <a name="texture2darraygathercmpsfloatfloatintuint-function"></a>Funzione Texture2DArray::GatherCmp(S,float,float,int,uint)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto con un valore di confronto insieme allo stato del mapping dei riquadri.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
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

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Offset applicato alle coordinate della trama prima del campionamento.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

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

[Metodi GatherCmp](texture2darray-gathercmp.md)
</dt> </dl>

 

 
