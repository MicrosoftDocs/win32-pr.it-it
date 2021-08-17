---
title: Funzione TextureCubeArray::Sample(S,float,float)
description: Campionare una trama con un valore facoltativo in cui impostare i valori di livello di dettaglio (LOD) del campione. | Funzione TextureCubeArray::Sample(S,float,float)
ms.assetid: E3BACA5E-18FC-4BD7-A8D8-C2808BDF1517
keywords:
- Funzione di esempio HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3341401c67f534e68b2262c73d8a74ee851f0ec3bea11574011226165056805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723326"
---
# <a name="texturecubearraysamplesfloatfloat-function"></a>Funzione TextureCubeArray::Sample(S,float,float)

Campionare una trama con un valore facoltativo in cui impostare i valori di livello di dettaglio (LOD) del campione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Tipo: **SamplerState**

Stato [del campionatore.](dx-graphics-hlsl-sampler.md) Si tratta di un oggetto dichiarato in un file di effetti che contiene assegnazioni di stato.

</dd> <dt>

*Posizione* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Coordinate di trama. Il tipo di argomento dipende dal tipo texture-object.



| Texture-Object tipo                    | Tipo di parametro |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Clamp* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore facoltativo in cui impostare i valori loD di esempio. Ad esempio, se si passa 2.0f per il valore di chiusura, si garantisce che nessun singolo campione accerta un livello mip inferiore a 2,0f.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Il formato della trama, che è uno dei valori tipiati elencati in [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di esempio](texturecubearray-sample.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
