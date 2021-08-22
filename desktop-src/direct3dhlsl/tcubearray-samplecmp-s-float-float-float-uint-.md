---
title: Funzione SampleCmp::SampleCmp(S,float,float,float,uint) per TextureCubeArray
description: Campionare una trama, usando un valore di confronto per rifiutare i campioni, con un valore facoltativo a cui stringere i valori del livello di dettaglio del campione. | Funzione SampleCmp::SampleCmp(S,float,float,float,uint) per TextureCubeArray
ms.assetid: 5596D341-C057-414D-B1EC-7AA78693D32C
keywords:
- Funzione SampleCmp HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0842296ad5f7f4dd85be50c6be6f7e4b9c24c9bc99b00fda0c7f4fb376d8a768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043095"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecubearray"></a>Funzione SampleCmp::SampleCmp(S,float,float,float,uint) per TextureCubeArray

Campionare una trama, usando un valore di confronto per rifiutare i campioni, con un valore facoltativo a cui stringere i valori del livello di dettaglio del campione. Restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Tipo: **SamplerState**

Stato [del campionatore.](dx-graphics-hlsl-sampler.md) Si tratta di un oggetto dichiarato in un file di effetto che contiene assegnazioni di stato.

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

*CompareValue* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore a virgola mobile da usare come valore di confronto.

</dd> <dt>

*Clamp* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore facoltativo a cui impostare i valori LOD di esempio. Ad esempio, se si passa 2.0f per il valore clamp, si garantisce che nessun singolo campione accerta un livello mip inferiore a 2,0f.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE** se tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati prelevati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato della trama, ovvero uno dei valori tipi di dati elencati in [**FORMATO DXGI. \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi SampleCmp](texturecubearray-samplecmp.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
