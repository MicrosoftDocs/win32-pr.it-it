---
description: Crea un oggetto mesh usando un codice FVF (Flexible Vertex Format).
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: Funzione D3DXCreateMeshFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323548"
---
# <a name="d3dxcreatemeshfvf-function"></a>D3DXCreateMeshFVF (funzione)

Crea un oggetto mesh usando un codice FVF (Flexible Vertex Format).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumFaces* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di visi per la mesh. L'intervallo valido per questo numero è maggiore di 0 e uno minore del valore DWORD massimo, in genere 2 ³ ²-1, perché l'ultimo indice è riservato.

</dd> <dt>

*NumVertices* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici per la mesh. Questo parametro deve essere maggiore di 0.

</dd> <dt>

*Opzioni* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) , che specifica le opzioni di creazione per la mesh.

</dd> <dt>

*FVF* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di [D3DFVF](d3dfvf.md) che descrive il formato del vertice per la mesh restituita. Questa funzione non supporta D3DFVF \_ XYZRHW.

</dd> <dt>

*pD3DDevice* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo da associare alla mesh.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta l'oggetto mesh creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
