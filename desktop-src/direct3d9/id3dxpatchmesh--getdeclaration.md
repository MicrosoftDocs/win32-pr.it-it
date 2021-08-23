---
description: 'Metodo ID3DXPatchMesh::GetDeclaration: ottiene la dichiarazione dei vertici.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: Metodo ID3DXPatchMesh::GetDeclaration (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 120a9f4179819b550502c2c3764d334159b647fd4c8621d3a088516b9a669d56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747851"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>Metodo ID3DXPatchMesh::GetDeclaration

Ottiene la dichiarazione del vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeclaration* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrivono il formato dei vertici della mesh. La dimensione di questa matrice di dichiaratori è [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md). La matrice di elementi vertice termina con la macro [**D3DDECL \_ END.**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

La matrice di elementi include la macro [**D3DDECL \_ END,**](d3ddecl-end.md) che termina la dichiarazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
