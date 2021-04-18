---
description: Calcolare gli IMT per triangolo da dati per vertice. Questa funzione consente di calcolare l'IMT in base a qualsiasi valore in una mesh (colore, normale e così via).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Funzione D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322866"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>D3DXComputeIMTFromPerVertexSignal (funzione)

Calcolare gli IMT per triangolo da dati per vertice. Questa funzione consente di calcolare l'IMT in base a qualsiasi valore in una mesh (colore, normale e così via).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo di IMT.

</dd> <dt>

*pfVertexSignal* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di dati per vertice da cui verrà calcolato IMT. La dimensione della matrice è uSignalStride \* v, dove v è il numero di vertici nella rete.

</dd> <dt>

*uSignalDimension* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di float per vertice.

</dd> <dt>

*uSignalStride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di byte per vertice nella matrice. Deve essere un multiplo di sizeof (float)

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di incapsulamento della trama. Si tratta di una combinazione di uno o più [**flag D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Puntatore a una funzione di callback per monitorare lo stato di avanzamento del calcolo di IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato. Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.

</dd> <dt>

*ppIMTData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita. Questa matrice può essere fornita come input per le [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) di D3DX per definire la priorità dell'allocazione dello spazio di trama nella parametrizzazione della trama.

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
</dt> <dt>

[Uso di UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
