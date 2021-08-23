---
title: Funzione SampleBias::SampleBias(S,float,float,float) per TextureCubeArray
description: La funzione SampleBias::SampleBias(S,float,float,float) per TextureCubeArray campionare una trama, dopo aver applicato il valore di distorsione al livello mipmap.
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
keywords:
- Funzione SampleBias HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea7c030ca1a99e9d9169ac4e20c26fbb352d199f471be2f926f758c87374b092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043135"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a>Funzione SampleBias::SampleBias(S,float,float,float) per TextureCubeArray

Campionare una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo a cui applicare i valori di livello di dettaglio (LOD) del campione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
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

*Distorsione* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusi, viene applicato a un livello mip prima del campionamento.

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

[Metodi di SampleBias](texturecubearray-samplebias.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
