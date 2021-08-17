---
title: Funzione SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) per Texture2DArray
description: Viene eseguito il campionamento di una trama solo sul livello mipmap 0 e il risultato viene confrontato con un valore di confronto e quindi viene restituito lo stato dell'operazione. Per Texture2DArray.
ms.assetid: 2F5669A6-D506-4096-A37E-421E5A16545F
keywords:
- Funzione SampleCmpLevelZero HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6100fc2a801aa3df8d4b86f07b387da6c1fc4aaf33cfbea52bff0bfb632f213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507374"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture2darray"></a>Funzione SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) per Texture2DArray

Viene eseguito il campionamento di una trama solo sul livello mipmap 0 e il risultato viene confrontato con un valore di confronto. Restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
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

Stato [del campionatore.](dx-graphics-hlsl-sampler.md) Si tratta di un oggetto dichiarato in un file di effetti che contiene assegnazioni di stato.

</dd> <dt>

*Località* \[ Pollici\]
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

*CompareValue* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore a virgola mobile da utilizzare come valore di confronto.

</dd> <dt>

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento. Usare un offset solo in corrispondenza di un valore integer miplevel. In caso contrario, è possibile ottenere risultati che non vengono tradotti bene in hardware. Il tipo di argomento dipende dal tipo texture-object. Per altre informazioni, vedere [Applicazione di offset di interi.](dx-graphics-hlsl-to-sample.md)



| Texture-Object tipo           | Tipo di parametro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non supportato  |



 

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Il formato della trama, che è uno dei valori tipiati elencati in [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi sampleCmpLevelZero](texture2darray-samplecmplevelzero.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
