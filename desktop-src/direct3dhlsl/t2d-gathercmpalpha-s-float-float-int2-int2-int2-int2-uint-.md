---
title: Funzione Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2,uint)
description: Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto del relativo componente alfa con un valore di confronto insieme allo stato del mapping delle sezioni. | Funzione Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2,uint)
ms.assetid: 4DB56BE2-503A-4D51-89FB-E4DD91EBF028
keywords:
- Funzione GatherCmpAlpha HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4db53509411c4b0d8e189f7ec9e2e3a1bee0fa7fa14fee94a7d5cc60a0703743
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118141"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2uint-function"></a>Funzione Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2,uint)

Per quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, restituisce un confronto del relativo componente alfa con un valore di confronto insieme allo stato del mapping delle sezioni.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

[Metodi GatherCmpAlpha](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 
