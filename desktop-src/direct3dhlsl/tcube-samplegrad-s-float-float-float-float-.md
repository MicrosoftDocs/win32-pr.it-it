---
title: Funzione SampleGrad::SampleGrad(S,float,float,float,float) per TextureCube
description: Campionare una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione, con un valore facoltativo a cui stringere i valori del livello di dettaglio (LOD) del campione. Per TextureCube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
keywords:
- Funzione SampleGrad HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebaa411ccb6075cfe9aab429912c3644c50e2c8bf1db99faec3328f318700268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043299"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a>Funzione SampleGrad::SampleGrad(S,float,float,float,float) per TextureCube

Campionare una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione, con un valore facoltativo a cui stringere i valori del livello di dettaglio (LOD) del campione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Tipo: **SamplerState**

Stato [del campionatore.](dx-graphics-hlsl-sampler.md) Si tratta di un oggetto dichiarato in un file degli effetti che contiene assegnazioni di stato.

</dd> <dt>

*Località* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Coordinate di trama. Il tipo di argomento dipende dal tipo di oggetto trama.



| tipo Texture-Object                    | Tipo di parametro |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*DDX* \[ in\]
</dt> <dd>

Tipo: **float**

Frequenza di modifica della geometria della superficie nella direzione x. Il tipo di argomento dipende dal tipo di oggetto trama.



| tipo Texture-Object                      | Tipo di parametro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | non supportato  |



 

</dd> <dt>

*DDY* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Frequenza di modifica della geometria della superficie nella direzione y. Il tipo di argomento dipende dal tipo di oggetto trama.



| tipo Texture-Object                      | Tipo di parametro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | non supportato  |



 

</dd> <dt>

*Clamp* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore facoltativo a cui stringere i valori LOD di esempio. Ad esempio, se si passa 2.0f per il valore clamp, si garantisce che nessun singolo campione accerta un livello mip inferiore a 2,0f.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato della trama, ovvero uno dei valori tipi di dati elencati in [**FORMATO DXGI. \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi SampleGrad](texturecube-samplegrad.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
