---
description: Genera un nuovo mapping del vertice ottimizzato per un elenco di triangolo. Questa funzione viene in genere utilizzata dopo l'applicazione del nuovo mapping della faccia generato da D3DXOptimizeFaces.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: Funzione D3DXOptimizeVertices (D3DX9Mesh. h)
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
ms.openlocfilehash: 734c2224ae29e7ab166010d59859d00355e5400e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322120"
---
# <a name="d3dxoptimizevertices-function"></a>D3DXOptimizeVertices (funzione)

Genera un nuovo mapping del vertice ottimizzato per un elenco di triangolo. Questa funzione viene in genere utilizzata dopo l'applicazione del nuovo mapping della faccia generato da [**D3DXOptimizeFaces**](d3dxoptimizefaces.md).

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

*pIndices* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore agli indici di elenco di triangolo da usare per l'ordinamento dei vertici.

</dd> <dt>

*NumFaces* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di visi nell'elenco dei triangoli.

</dd> <dt>

*NumVertices* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vertici a cui fa riferimento l'elenco dei triangoli.

</dd> <dt>

*Indices32Bit* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Flag che indica il tipo di indice: **true** se gli indici sono a 32 bit (più di 65535 vertici); **false** se gli indici sono a 16 bit (65535 o meno vertici).

</dd> <dt>

*pVertexRemap* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a un buffer di destinazione che conterrà il nuovo indice per ogni vertice. Il valore archiviato in *pVertexRemap* per un dato elemento è la posizione del vertice di origine nell'ordinamento del nuovo vertice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, una mesh Usa indici a 16 bit quando viene creato, a meno che l'applicazione non specifichi diversamente. Per verificare se una mesh esistente Usa indici a 16 bit o a 32 bit, chiamare [**ID3DXBaseMesh:: GetOptions**](id3dxbasemesh--getoptions.md) e verificare la presenza del flag D3DXMESH a \_ 32 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
