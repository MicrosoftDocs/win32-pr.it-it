---
title: Funzione SampleGrad::SampleGrad(S,float,float,float,int,float) per Texture2DArray
description: Informazioni su come questa funzione campionare una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione, con un valore facoltativo a cui impostare i valori del livello di dettaglio (LOD) del campione. Per Texture2DArray.
ms.assetid: CBC940D5-FC09-498D-9C7A-3CBAB2EC2D4D
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
ms.openlocfilehash: abb3b714622550315a714b314772f7002872ee71863e12db234db4b6794aeadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043439"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2darray"></a>Funzione SampleGrad::SampleGrad(S,float,float,float,int,float) per Texture2DArray

Campionare una trama, usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione, con un valore facoltativo a cui stringere i valori del livello di dettaglio (LOD) del campione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
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

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento. Usare un offset solo in corrispondenza di un valore integer miplevel; In caso contrario, è possibile che si otterrà un risultato che non si traduce bene in hardware. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere [Applicazione di offset di interi.](dx-graphics-hlsl-to-sample.md)



| tipo Texture-Object           | Tipo di parametro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non supportato  |



 

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

[Metodi SampleGrad](texture2darray-samplegrad.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
