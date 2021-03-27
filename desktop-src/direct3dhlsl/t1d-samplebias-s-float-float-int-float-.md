---
title: 'Funzione SampleBias:: SampleBias (S, float, float, int, float)'
description: 'Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a. | Funzione SampleBias:: SampleBias (S, float, float, int, float)'
ms.assetid: 88BC4E99-B33D-4DAA-9A77-849B2F5FE6A7
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
ms.openlocfilehash: 3af7ddaf3c015c2254761cce1d7cd30a2a68629b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995525"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a>Funzione SampleBias:: SampleBias (S, float, float, int, float)

Esegue il campionamento di una trama, dopo aver applicato il valore di distorsione al livello mipmap, con un valore facoltativo per limitare i valori del livello di dettaglio (LOD) campione a.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
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

*Distorsione* \[ in\]
</dt> <dd>

Tipo: **float**

Il valore di distorsione, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusivo, viene applicato a un livello MIP prima del campionamento.

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

[Metodi SampleBias](texture1d-samplebias.md)
</dt> </dl>

 

 
