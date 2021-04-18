---
description: Recupera una dichiarazione che descrive i vertici nella mesh.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: 'Metodo ID3DXBaseMesh:: getDeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f8736e822bfe4a959f35f60bb79783e79f2d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322068"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a>Metodo ID3DXBaseMesh:: getDeclaration

Recupera una dichiarazione che descrive i vertici nella mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dichiarazione* \[ di in uscita\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato del vertice dei vertici della mesh. Il limite superiore della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md). La matrice di elementi Vertex termina con la macro [**D3DDECL \_ end**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

La matrice di elementi include la macro [**D3DDECL \_ end**](d3ddecl-end.md) , che termina la dichiarazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
