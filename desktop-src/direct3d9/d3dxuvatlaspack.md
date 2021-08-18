---
description: Creare un pacchetto di dati di partizionamento mesh in un atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Funzione D3DXUVAtlasPack (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6990d6fbc114c874b31d0035a2415d48161d3065718efce3783a041a2097e96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749661"
---
# <a name="d3dxuvatlaspack-function"></a>Funzione D3DXUVAtlasPack

Creare un pacchetto di dati di partizionamento mesh in un atlas.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh)**](id3dxmesh.md)che contiene la geometria dell'oggetto per il calcolo dell'at atlas. Come minimo, la mesh deve contenere dati di posizione e coordinate di trama 2D.

</dd> <dt>

*dwWidth* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Larghezza della trama.

</dd> <dt>

*dwHeight* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altezza della trama.

</dd> <dt>

*fGutter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distanza minima, in texel, tra due grafici sull'at atlas. La barra di margine viene sempre ridimensionata in base alla larghezza; Pertanto, se viene usato un margine di 2,5 su una trama 512x512, la distanza minima tra due grafici è 2,5 / 512,0 texel.

</dd> <dt>

*dwTextureIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice delle coordinate della trama in base zero che identifica il set di coordinate di trama da usare.

</dd> <dt>

*pdwPartitionResultAdjacency* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh. Deve essere derivato da ppPartitionResultAdjacency restituito da [**D3DXUVAtlasPartition.**](d3dxuvatlaspartition.md) Questo valore non può **essere NULL** perché Pack deve sapere dove sono stati tagliati i grafici nel passaggio della partizione per trovare i bordi di ogni grafico.

</dd> <dt>

*pCallback* \[ Pollici\]
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Puntatore a una funzione di callback (vedere [LPD3DXUVATLASCB)](lpd3dxuvatlascb.md)utile per monitorare lo stato di avanzamento.

</dd> <dt>

*fCallbackFrequency* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Specificare la frequenza con cui D3DX chiamerà il callback. un valore predefinito ragionevole è 0,0001f.

</dd> <dt>

*pUserContent* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore void da passare nuovamente alla funzione di callback.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Questo parametro options è attualmente riservato.

</dd> <dt>

*pFacePartitioning* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntatore a un [**OGGETTO ID3DXBuffer**](id3dxbuffer.md) contenente la matrice del partizionamento viso finale. Ogni elemento contiene un valore DWORD per ogni viso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D OK; in caso contrario, il valore \_ è D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
