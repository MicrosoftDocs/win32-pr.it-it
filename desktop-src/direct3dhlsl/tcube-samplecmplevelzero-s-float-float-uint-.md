---
title: Funzione SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) per TextureCube
description: Viene eseguito il campionamento di una trama solo sul livello mipmap 0 e il risultato viene confrontato con un valore di confronto. Restituisce lo stato dell'operazione. Per TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
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
ms.openlocfilehash: 5970b2a03a3004269b8ef758569aa6ac222bb60032dcb91e121a342e58cef886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117991"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a>Funzione SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) per TextureCube

Viene eseguito il campionamento di una trama solo sul livello mipmap 0 e il risultato viene confrontato con un valore di confronto. Restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
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

[Metodi sampleCmpLevelZero](texturecube-samplecmplevelzero.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
