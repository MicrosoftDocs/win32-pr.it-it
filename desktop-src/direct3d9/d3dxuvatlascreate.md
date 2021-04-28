---
description: 'Funzione D3DXUVAtlasCreate: consente di creare un at atlas UV per una mesh.'
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Funzione D3DXUVAtlasCreate (D3DX9Mesh.h)
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
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117829"
---
# <a name="d3dxuvatlascreate-function"></a>Funzione D3DXUVAtlasCreate

Creare un at atlas UV per una mesh.

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

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh)**](id3dxmesh.md)che contiene la geometria dell'oggetto per il calcolo dell'at atlas. Come minimo, la mesh deve contenere dati di posizione e coordinate di trama 2D.

</dd> <dt>

*dwMaxChartNumber* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di grafici in cui partizionare la mesh. Vedere le osservazioni sulle modalità di partizionamento. Usare 0 per indicare a D3DX che l'atlas deve essere parametrizzato in base all'estensione.

</dd> <dt>

*fMaxStretch* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Quantità di estensione consentita. 0 indica che non è consentita alcuna estensione, 1 indica che è possibile usare qualsiasi quantità di estensione.

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

Distanza minima, in texel, tra due grafici sull'at atlas. Il margine viene sempre ridimensionato in base alla larghezza. Pertanto, se viene usata una distanza di 2,5 su una trama 512x512, la distanza minima tra due grafici è 2,5/512,0 texel.

</dd> <dt>

*dwTextureIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice delle coordinate della trama in base zero che identifica il set di coordinate di trama da usare.

</dd> <dt>

*pdwAdjacency* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di dati di adienza. con 3 DWORD per ogni viso, che indica quali triangoli sono adiacenti tra loro (vedere [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matrice con 3 DWORD per ogni viso. Ogni viso indica se un bordo è falso o meno. Un bordo non falso è indicato da -1, un bordo falso è indicato da qualsiasi altro valore. Ciò consente la parametrizzazione di una mesh di quad in cui i bordi al centro di ogni quad non verranno tagliati.

</dd> <dt>

*pfIMTArray* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tensori delle metriche integrati che descrive come estendere un triangolo (vedere [IntegratedMetricTensor).](using-uvatlas.md)

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

Puntatore a un valore definito dall'utente passato alla funzione di callback. utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specificare la qualità dei grafici generati. Vedere [**D3DXUVATLAS.**](./d3dxuvatlas.md)

</dd> <dt>

*ppMeshOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntatore alla mesh creata con l'atlas (vedere [**ID3DXMesh).**](id3dxmesh.md)

</dd> <dt>

*PpFacePartitioning* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a una matrice dei dati finali di partizionamento viso. Ogni elemento contiene un valore DWORD per ogni viso (vedere [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a una matrice di vertici mappati. Ogni elemento della matrice identifica il vertice originale da cui deriva ogni vertice finale (se il vertice è stato suddiviso durante il mapping). Ogni elemento della matrice contiene un valore DWORD per vertice.

</dd> <dt>

*pfMaxStretchOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al valore di estensione massimo generato dall'algoritmo Atlas. L'intervallo è compreso tra 0,0 e 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore al numero di grafici creati dall'algoritmo Atlas. Se dwMaxChartNumber è troppo basso, questo parametro restituirà il numero minimo di grafici necessari per creare un at atlas.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D OK; in caso contrario, il valore \_ è D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

D3DXUVAtlasCreate può partizionare la geometria della mesh in due modi:

-   In base al numero di grafici
-   In base all'estensione massima consentita. Se l'estensione massima consentita è 0, è probabile che ogni triangolo si trova nel proprio grafico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
