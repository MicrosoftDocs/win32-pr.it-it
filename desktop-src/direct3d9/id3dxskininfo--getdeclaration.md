---
description: 'Metodo ID3DXSkinInfo::GetDeclaration: ottiene la dichiarazione del vertice.'
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: Metodo ID3DXSkinInfo::GetDeclaration (D3DX9Mesh.h)
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
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093139"
---
# <a name="id3dxskininfogetdeclaration-method"></a>Metodo ID3DXSkinInfo::GetDeclaration

Ottiene la dichiarazione del vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dichiarazione* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrivono il formato dei vertici della mesh. Il limite superiore di questa matrice di dichiaratori è [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md). La matrice di elementi vertice termina con la macro [**D3DDECL \_ END.**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

La matrice di elementi include la macro [**D3DDECL \_ END,**](d3ddecl-end.md) che termina la dichiarazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetDeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
