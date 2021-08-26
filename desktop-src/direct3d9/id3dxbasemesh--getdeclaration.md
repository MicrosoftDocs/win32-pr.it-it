---
description: Recupera una dichiarazione che descrive i vertici nella mesh.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: Metodo ID3DXBaseMesh::GetDeclaration (D3DX9Mesh.h)
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
ms.openlocfilehash: 4d66afd8daf6a8cc60fa63dcf38e6bb853c33ca05986d2a37b94eba1250eb01b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026471"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a>Metodo ID3DXBaseMesh::GetDeclaration

Recupera una dichiarazione che descrive i vertici nella mesh.

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

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
