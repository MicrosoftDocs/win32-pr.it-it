---
title: Funzione SampleLevel::SampleLevel(S,float,float,int,uint) per Texture2DArray
description: Campita una trama a livello di mipmap specificato e restituisce lo stato dell'operazione. Per Texture2DArray. | Funzione SampleLevel::SampleLevel(S,float,float,int,uint)
ms.assetid: 2A561EE4-D7CF-44D4-AC93-F6841770B868
keywords:
- Funzione SampleLevel HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b00882702b44b7d4f9ccb101866400cb023cea00be637e898d9ecd71ed2e262
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118051"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2darray"></a>Funzione SampleLevel::SampleLevel(S,float,float,int,uint) per Texture2DArray

Campita una trama a livello di mipmap specificato e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
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

*LOD* \[ Pollici\]
</dt> <dd>

Tipo: **float**

\[in \] Numero che specifica il livello mipmap. Se il valore è ≤ 0, viene usato il livello mipmap 0 (mappa principale). Il valore frazionario (se specificato) viene usato per eseguire l'interpolazione tra due livelli mipmap.

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

[Metodi di SampleLevel](texture2darray-samplelevel.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
