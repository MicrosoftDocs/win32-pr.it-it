---
title: 'Funzione SampleCmp:: SampleCmp (S, float, float, float) per TextureCubeArray'
description: 'Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in. | Funzione SampleCmp:: SampleCmp (S, float, float, float) per TextureCubeArray'
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
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
ms.openlocfilehash: e65b1747d03b3a0555267f7b57e95a4d5aba54da
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982643"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a>Funzione SampleCmp:: SampleCmp (S, float, float, float) per TextureCubeArray

Esegue il campionamento di una trama, usando un valore di confronto per rifiutare esempi, con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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

[Metodi SampleCmp](texturecubearray-samplecmp.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
