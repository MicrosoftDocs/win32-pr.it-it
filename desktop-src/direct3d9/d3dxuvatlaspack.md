---
description: Comprime i dati di partizionamento mesh in un Atlante.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Funzione D3DXUVAtlasPack (D3DX9Mesh. h)
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
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322569"
---
# <a name="d3dxuvatlaspack-function"></a>D3DXUVAtlasPack (funzione)

Comprime i dati di partizionamento mesh in un Atlante.

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

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo dell'Atlante. Come minimo, la mesh deve contenere dati sulla posizione e coordinate di trama 2D.

</dd> <dt>

*dwWidth* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Spessore trama.

</dd> <dt>

*dwHeight* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altezza trama.

</dd> <dt>

*fGutter* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distanza minima, in Texel, tra due grafici nell'Atlante. La gronda viene sempre ridimensionata in base alla larghezza; Se quindi si usa una gronda di 2,5 su una trama 512x512, la distanza minima tra due grafici è 2,5/512,0 Texels.

</dd> <dt>

*dwTextureIndex* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.

</dd> <dt>

*pdwPartitionResultAdjacency* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh. Deve derivare da ppPartitionResultAdjacency restituito da [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md). Questo valore non può essere **null**, perché Pack deve sapere dove sono stati tagliati i grafici nel passaggio della partizione per trovare i bordi di ogni grafico.

</dd> <dt>

*pCallback* \[ in\]
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Puntatore a una funzione di callback (vedere [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) utile per il monitoraggio dello stato di avanzamento.

</dd> <dt>

*fCallbackFrequency* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Specificare la frequenza con cui D3DX chiamerà il callback; un valore predefinito ragionevole è 0,0001 f.

</dd> <dt>

*pUserContent* \[ in\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore void da passare di nuovo alla funzione di callback.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Questo parametro di opzioni è attualmente riservato.

</dd> <dt>

*pFacePartitioning* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntatore a un [**ID3DXBuffer**](id3dxbuffer.md) contenente la matrice del partizionamento finale della faccia. Ogni elemento contiene un valore DWORD per ogni faccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
