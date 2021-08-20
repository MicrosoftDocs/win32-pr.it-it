---
title: Funzione SampleBias::SampleBias(S,float,float,int,float,uint) per Texture2D
description: La funzione SampleBias::SampleBias(S,float,float,int,float,uint) consente di eseguire il campionamento di un oggetto Texture2D, dopo l'applicazione del valore di distorsione al livello mipmap.
ms.assetid: ACABF551-1DBF-4979-B0B1-D025E04EC08C
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
ms.openlocfilehash: a97861d19632bccb5b0994750cac9a11d044fcff2378932b62dedf4315feea80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906213"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2d"></a>Funzione SampleBias::SampleBias(S,float,float,int,float,uint) per Texture2D

Campionare [**un oggetto Texture2D**](sm5-object-texture2d.md)dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo a cui applicare i valori di livello di dettaglio (LOD) del campione. Restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
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

*Offset* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento. Usare un offset solo in corrispondenza di un valore integer miplevel. In caso contrario, è possibile ottenere risultati che non si traducono bene in hardware. Il tipo di argomento dipende dal tipo texture-object. Per altre informazioni, vedere [Applicazione di offset di interi.](dx-graphics-hlsl-to-sample.md)



| Texture-Object tipo           | Tipo di parametro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non supportato  |



 

</dd> <dt>

*Clamp* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Valore facoltativo in cui impostare i valori loD di esempio. Ad esempio, se si passa 2.0f per il valore di chiusura, si garantisce che nessun singolo campione accerta un livello mip inferiore a 2,0f.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE se** tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati presi valori da un riquadro non mappato, **CheckAccessFullyMapped restituisce** **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato della trama, che è uno dei valori tipiati elencati in [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di SampleBias](texture2d-samplebias.md)
</dt> </dl>

 

 
