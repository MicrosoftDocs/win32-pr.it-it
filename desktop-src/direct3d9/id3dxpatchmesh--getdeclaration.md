---
description: Ottiene la dichiarazione del vertice.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'Metodo ID3DXPatchMesh:: getDeclaration (D3DX9Mesh. h)'
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
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356084"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>Metodo ID3DXPatchMesh:: getDeclaration

Ottiene la dichiarazione del vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeclaration* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato del vertice dei vertici della mesh. La dimensione della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md). La matrice di elementi Vertex termina con la macro [**D3DDECL \_ end**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

La matrice di elementi include la macro [**D3DDECL \_ end**](d3ddecl-end.md) , che termina la dichiarazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
