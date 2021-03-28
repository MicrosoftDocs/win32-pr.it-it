---
title: 'Funzione SampleLevel:: SampleLevel (S, float, float, uint) per TextureCube'
description: "Esegue il campionamento di una trama sul livello mipmap specificato e restituisce lo stato dell'operazione. | Funzione SampleLevel:: SampleLevel (S, float, float, uint)"
ms.assetid: DB27D8B9-11AB-4F0C-947A-9469BA565F41
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
ms.openlocfilehash: a31eaa2351b4758c29327aaa08ccee5ed0c3056c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104402043"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function-for-texturecube"></a>Funzione SampleLevel:: SampleLevel (S, float, float, uint) per TextureCube

Esegue il campionamento di una trama sul livello mipmap specificato e restituisce lo stato dell'operazione.

## <a name="syntax"></a>Sintassi


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
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

*LOD* \[ in\]
</dt> <dd>

Tipo: **float**

\[in \] un numero che specifica il livello mipmap. Se il valore è ≤ 0, viene usato il livello mipmap 0 (mapping più grande). Il valore frazionario (se fornito) viene usato per interpolare tra due livelli di mipmap.

</dd> <dt>

*Stato* \[ di out\]
</dt> <dd>

Tipo: **uint**

Stato dell'operazione. Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features). Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi SampleLevel](texturecube-samplelevel.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
