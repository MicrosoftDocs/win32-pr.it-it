---
description: Convalida una mesh patch, restituendo il numero di vertici e patch degenerati.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Funzione D3DXValidPatchMesh (D3DX9Mesh. h)
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
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969335"
---
# <a name="d3dxvalidpatchmesh-function"></a>D3DXValidPatchMesh (funzione)

Convalida una mesh patch, restituendo il numero di vertici e patch degenerati.

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

*pMeshIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Puntatore a un'interfaccia [**ID3DXPatchMesh**](id3dxpatchmesh.md) , che rappresenta la mesh della patch da testare.

</dd> <dt>

*pNumDegenerateVertices* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Restituisce il numero di vertici degenerati nella mesh della patch.

</dd> <dt>

*pNumDegeneratePatches* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Restituisce il numero di patch degenerate nella mesh patch.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un puntatore a un buffer contenente una stringa di errori e avvisi che illustrano i problemi rilevati nella mesh della patch.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo convalida la mesh controllando la presenza di indici non validi. Le informazioni sull'errore sono disponibili nell'output del debugger.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
