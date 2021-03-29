---
title: 'Funzione SampleCmp:: SampleCmp (S, float, float, int, float) per Texture1D'
description: 'Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione SampleCmp:: SampleCmp (S, float, float, int, float) per Texture1D'
ms.assetid: 91AD0B59-D3F0-4A0D-8825-17282815D64B
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
ms.openlocfilehash: 811636e7e7002afedf026d4e3955f08f647c2c5d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996385"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture1d"></a>Funzione SampleCmp:: SampleCmp (S, float, float, int, float) per Texture1D

Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Tipo: **SamplerState**

[Stato del campionatore](dx-graphics-hlsl-sampler.md). Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.

</dd> <dt>

*Posizione* \[ in\]
</dt> <dd>

Tipo: **float**

Coordinate di trama. Il tipo di argomento dipende dal tipo di oggetto trama.



| Tipo di Texture-Object                    | Tipo di parametro |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*CompareValue* \[ in\]
</dt> <dd>

Tipo: **float**

Valore a virgola mobile da utilizzare come valore di confronto.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Tipo: **int**

Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento. Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati che non si traducono correttamente nell'hardware. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere [Applying Integer offsets](dx-graphics-hlsl-to-sample.md).



| Tipo di Texture-Object           | Tipo di parametro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non supportato  |



 

</dd> <dt>

*Blocca* \[ in\]
</dt> <dd>

Tipo: **float**

Valore facoltativo a cui bloccare i valori LOD di esempio. Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi SampleCmp](texture1d-samplecmp.md)
</dt> </dl>

 

 
