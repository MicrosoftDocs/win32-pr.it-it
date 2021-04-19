---
description: Creare un Atlante UV per una rete mesh.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Funzione D3DXUVAtlasCreate (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322468"
---
# <a name="d3dxuvatlascreate-function"></a>D3DXUVAtlasCreate (funzione)

Creare un Atlante UV per una rete mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo dell'Atlante. Come minimo, la mesh deve contenere dati sulla posizione e coordinate di trama 2D.

</dd> <dt>

*dwMaxChartNumber* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero massimo di grafici in cui partizionare la mesh. Vedere la sezione Osservazioni sulle modalità di partizionamento. Usare 0 per indicare a D3DX che l'Atlante deve essere parametrizzato in base all'estensione.

</dd> <dt>

*fMaxStretch* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Quantità di estensione consentita. 0 indica che non è consentita l'estensione. 1 indica che è possibile utilizzare qualsiasi estensione.

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

*pdwAdjacency* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di dati adiacenza. con 3 DWORD per faccia, che indicano i triangoli adiacenti tra loro (vedere [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matrice con 3 DWORD per faccia. Ogni volto indica se un bordo è false o no. Un bordo non false è indicato da-1, mentre un bordo false è indicato da un altro valore. In questo modo viene abilitata la parametrizzazione di una mesh di quad in cui i bordi al centro di ogni quad non vengono tagliati.

</dd> <dt>

*pfIMTArray* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tensori metrici integrati che descrive come estendere un triangolo (vedere [IntegratedMetricTensor](using-uvatlas.md)).

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

Puntatore a un valore definito dall'utente che viene passato alla funzione di callback; usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Consente di specificare la qualità dei grafici generati. Vedere [**D3DXUVATLAS**](./d3dxuvatlas.md).

</dd> <dt>

*ppMeshOut* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntatore alla mesh creata con Atlas (vedere [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*ppFacePartitioning* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a una matrice dei dati finali di partizionamento delle facce. Ogni elemento contiene un valore DWORD per faccia (vedere [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a una matrice di vertici di cui è stato eseguito il mapping. Ogni elemento della matrice identifica il vertice originale da cui provengono ogni vertice finale (se il vertice è stato suddiviso durante la modifica del mapping). Ogni elemento di matrice contiene un valore DWORD per vertice.

</dd> <dt>

*pfMaxStretchOut* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al valore di estensione massimo generato dall'algoritmo Atlas. L'intervallo è compreso tra 0,0 e 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore al numero di grafici creato dall'algoritmo Atlas. Se dwMaxChartNumber è troppo basso, questo parametro restituirà il numero minimo di grafici necessari per creare un Atlante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

D3DXUVAtlasCreate può partizionare la geometria mesh in due modi:

-   In base al numero di grafici
-   In base all'estensione massima consentita. Se l'estensione massima consentita è 0, è probabile che ogni triangolo si trovi in un grafico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Strumento Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
