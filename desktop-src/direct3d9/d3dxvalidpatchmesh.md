---
description: Convalida una mesh di patch, che restituisce il numero di vertici e patch degenerati.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Funzione D3DXValidPatchMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c3b7b28c763691af83dbb1ed0fe406fa6d370c82f9d8ffa702afa69566f2597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523813"
---
# <a name="d3dxvalidpatchmesh-function"></a>Funzione D3DXValidPatchMesh

Convalida una mesh di patch, che restituisce il numero di vertici e patch degenerati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMeshIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Puntatore a [**un'interfaccia ID3DXPatchMesh,**](id3dxpatchmesh.md) che rappresenta la mesh di patch da testare.

</dd> <dt>

*pNumDegenerateVertices* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Restituisce il numero di vertici degenerati nella mesh patch.

</dd> <dt>

*pNumDegeneratePatches* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Restituisce il numero di patch degenerate nella mesh delle patch.

</dd> <dt>

*ppErrorsAndWarnings* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un puntatore a un buffer contenente una stringa di errori e avvisi che illustrano i problemi rilevati nella mesh di patch.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo convalida la mesh controllando la presenza di indici non validi. Le informazioni sugli errori sono disponibili nell'output del debugger.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
