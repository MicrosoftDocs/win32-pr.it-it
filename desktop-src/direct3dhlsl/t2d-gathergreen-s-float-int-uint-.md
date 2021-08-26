---
title: Funzione Texture2D::GatherGreen(S,float,int,uint)
description: Restituisce i componenti verdi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, insieme allo stato del mapping delle sezioni. | Funzione Texture2D::GatherGreen(S,float,int,uint)
ms.assetid: A50C41BC-FDF4-47E6-9776-F51B2B634713
keywords:
- Funzione GatherGreen HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5a0e0f081562f473a5333b0e5ba8201bcf618f7fa38a51c6574036be0a67e9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067521"
---
# <a name="texture2dgathergreensfloatintuint-function"></a>Funzione Texture2D::GatherGreen(S,float,int,uint)

Restituisce i componenti verdi dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, insieme allo stato del mapping delle sezioni.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
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

*Località* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Coordinate di esempio (u,v).

</dd> <dt>

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Offset applicato alle coordinate della trama prima del campionamento.

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

[Metodi GatherGreen](texture2d-gathergreen.md)
</dt> </dl>

 

 
