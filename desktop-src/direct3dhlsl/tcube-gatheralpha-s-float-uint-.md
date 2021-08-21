---
title: Funzione TextureCube::GatherAlpha(S,float,uint)
description: Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, insieme allo stato del mapping dei riquadri. | Funzione TextureCube::GatherAlpha(S,float,uint)
ms.assetid: 19BD3024-D3E5-4AEA-8C8E-510A4EB527B5
keywords:
- Funzione GatherAlpha HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3bda4a6c3144d18e4253ea767427804ca92e8f1c5161c5c9371db749db40fd8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043419"
---
# <a name="texturecubegatheralphasfloatuint-function"></a>Funzione TextureCube::GatherAlpha(S,float,uint)

Restituisce i componenti alfa dei quattro valori texel che verrebbero usati in un'operazione di filtro bi-lineare, insieme allo stato del mapping dei riquadri.

## <a name="syntax"></a>Sintassi


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
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

[Metodi GatherAlpha](texturecube-gatheralpha.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
