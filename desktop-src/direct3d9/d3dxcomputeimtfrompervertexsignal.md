---
description: Calcolare i valori IMT per triangolo dai dati per vertice. Questa funzione consente di calcolare l'IMT in base a qualsiasi valore in una mesh (colore, normale e così via).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Funzione D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh.h)
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
ms.openlocfilehash: 41d635bf436e139e4c44db75b1057cebc3a50cfee114a35bfc75a9de84abc404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299458"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>Funzione D3DXComputeIMTFromPerVertexSignal

Calcolare i valori IMT per triangolo dai dati per vertice. Questa funzione consente di calcolare l'IMT in base a qualsiasi valore in una mesh (colore, normale e così via).

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

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a una mesh di input (vedere [**ID3DXMesh)**](id3dxmesh.md)che contiene la geometria dell'oggetto per il calcolo dell'IMT.

</dd> <dt>

*pfVertexSignal* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di dati per vertice da cui verrà calcolato IMT. La dimensione della matrice è uSignalStride \* v, dove v è il numero di vertici nella mesh.

</dd> <dt>

*uSignalDimension* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di float per vertice.

</dd> <dt>

*uSignalStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di byte per vertice nella matrice. Deve essere un multiplo di sizeof(float)

</dd> <dt>

*dwOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opzioni di ritorno a capo automatico della trama. Si tratta di una combinazione di uno o più [**FLAG D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Puntatore a una funzione di callback per monitorare lo stato del calcolo IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato. Utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback.

</dd> <dt>

*ppIMTData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita. Questa matrice può essere fornita come input per le funzioni [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) D3DX per classificare in ordine di priorità l'allocazione dello spazio della trama nella parametrizzazione della trama.

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
</dt> <dt>

[Uso di UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
