---
title: Funzione TextureCubeArray::GatherCmp(S,float,float,uint)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto con un valore di confronto insieme allo stato del mapping dei riquadri. | Funzione TextureCubeArray::GatherCmp(S,float,float,uint)
ms.assetid: 758CD159-58B6-42AE-92B3-5AA3C72FD0F1
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
ms.openlocfilehash: c408185cfac58e27cd5911296285273885cc76a31240ac03532ae87b75718c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506566"
---
# <a name="texturecubearraygathercmpsfloatfloatuint-function"></a>Funzione TextureCubeArray::GatherCmp(S,float,float,uint)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto con un valore di confronto insieme allo stato del mapping dei riquadri.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

[Metodi GatherCmp](texturecubearray-gathercmp.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
