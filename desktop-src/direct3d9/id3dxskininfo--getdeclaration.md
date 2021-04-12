---
description: Ottiene la dichiarazione del vertice.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'Metodo ID3DXSkinInfo:: getDeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354064"
---
# <a name="id3dxskininfogetdeclaration-method"></a>Metodo ID3DXSkinInfo:: getDeclaration

Ottiene la dichiarazione del vertice.

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

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: sedichiarazione**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
