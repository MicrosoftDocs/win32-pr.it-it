---
description: 'Funzione D3DXUVAtlasPartition: crea un at atlas UV per una mesh.'
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Funzione D3DXUVAtlasPartition (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117799"
---
# <a name="d3dxuvatlaspartition-function"></a>Funzione D3DXUVAtlasPartition

Creare un at atlas UV per una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
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

*dwTextureIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice delle coordinate della trama in base zero che identifica il set di coordinate di trama da usare.

</dd> <dt>

*pdwAdjacency* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di dati di adiacenza con 3 DWORD per viso, che indica quali triangoli sono adiacenti l'uno all'altro (vedere [**ID3DXBaseMesh::GenerateAdjacency).**](id3dxbasemesh--generateadjacency.md)

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matrice con 3 DWORD per viso. Ogni viso indica se un bordo è false o meno. Un bordo non false è indicato da -1, un bordo falso è indicato da qualsiasi altro valore. Ciò consente la parametrizzazione di una mesh di quad in cui i bordi al centro di ogni quad non verranno tagliati.

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

Puntatore a un valore definito dall'utente passato alla funzione di callback. in genere usato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specificare la qualità dei grafici generati combinando uno o più flag [**D3DXUVATLAS.**](./d3dxuvatlas.md)

</dd> <dt>

*ppMeshOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntatore alla mesh creata con l'at atlas (vedere [**ID3DXMesh).**](id3dxmesh.md)

</dd> <dt>

*pFacePartitioning* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntatore a una matrice dei dati finali di partizionamento del viso. Ogni elemento contiene un valore DWORD per ogni viso (vedere [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a una matrice di vertici di cui è stato ridefinito il mapping. Ogni elemento della matrice identifica il vertice originale da cui deriva ogni vertice finale (se il vertice è stato suddiviso durante il nuovo mapping). Ogni elemento della matrice contiene un valore DWORD per vertice.

</dd> <dt>

*ppPartitionResultAdjacency* 
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Questo buffer conterrà una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh di output. Questo parametro non deve essere **NULL** perché la chiamata successiva a D3DXUVAtlasPack() lo richiede.

</dd> <dt>

*pfMaxStretchOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al valore di estensione massimo generato dall'algoritmo Atlas. L'intervallo è compreso tra 0,0 e 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore al numero di grafici creati dall'algoritmo Atlas. Se dwMaxChartNumber è troppo basso, questo parametro restituirà il numero minimo di grafici necessari per creare un atlas.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D OK; in caso contrario, il valore \_ è D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

D3DXUVAtlasPartition è simile a [**D3DXUVAtlasCreate,**](d3dxuvatlascreate.md)ad eccezione del fatto che D3DXUVAtlasPartition non esegue il passaggio di creazione del pacchetto finale.

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

 

 
