---
description: Genera un nuovo mapping dei vertici ottimizzato per un elenco di triangoli. Questa funzione viene comunemente usata dopo l'applicazione del nuovo mapping dei visi generato da D3DXOptimizeFaces.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: Funzione D3DXOptimizeVertices (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a60d7d47e78cd197a7bfcf6285509c9187e32e074347f63f8e76ef9ef866adfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044799"
---
# <a name="d3dxoptimizevertices-function"></a>Funzione D3DXOptimizeVertices

Genera un nuovo mapping dei vertici ottimizzato per un elenco di triangoli. Questa funzione viene comunemente usata dopo l'applicazione del nuovo mapping dei visi generato da [**D3DXOptimizeFaces**](d3dxoptimizefaces.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIndices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore agli indici dell'elenco triangolare da usare per l'ordinamento dei vertici.

</dd> <dt>

*NumFaces* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di visi nell'elenco di triangoli.

</dd> <dt>

*NumVertices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici a cui fa riferimento l'elenco di triangoli.

</dd> <dt>

*Indices32Bit* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Flag che indica il tipo di indice: **TRUE** se gli indici sono a 32 bit (più di 65535 vertici), **FALSE** se gli indici sono a 16 bit (65535 o meno vertici).

</dd> <dt>

*pVertexRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a un buffer di destinazione che conterrà il nuovo indice per ogni vertice. Il valore archiviato in *pVertexRemap per* un determinato elemento è la posizione del vertice di origine nel nuovo ordinamento dei vertici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, una mesh usa indici a 16 bit quando viene creata, a meno che l'applicazione non specifichi diversamente. Per verificare se una mesh esistente usa indici a 16 o a 32 bit, chiamare [**ID3DXBaseMesh::GetOptions**](id3dxbasemesh--getoptions.md) e verificare la presenza del flag D3DXMESH \_ a 32 BIT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
