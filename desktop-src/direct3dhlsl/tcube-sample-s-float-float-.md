---
title: Funzione TextureCube::Sample(S,float,float)
description: Campionare una trama con un valore facoltativo a cui impostare i valori del livello di dettaglio del campione. | Funzione TextureCube::Sample(S,float,float)
ms.assetid: 7DB25135-46B5-48E2-91D0-A45D355179D6
keywords:
- Funzione di esempio HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08613bb9b9465f1908828025316018d1747b1b0f7805478ce535457e45a2be18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788173"
---
# <a name="texturecubesamplesfloatfloat-function"></a>Funzione TextureCube::Sample(S,float,float)

Campionare una trama con un valore facoltativo a cui impostare i valori del livello di dettaglio del campione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
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

[Metodi di esempio](texturecube-sample.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
