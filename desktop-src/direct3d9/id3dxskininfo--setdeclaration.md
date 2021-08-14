---
description: Imposta la dichiarazione di vertice.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: Metodo ID3DXSkinInfo::SetDeclaration (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d7189abac9041e1abad67ea60558f5ec33714ae47d50225d362ad3bc09e6d1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985261"
---
# <a name="id3dxskininfosetdeclaration-method"></a>Metodo ID3DXSkinInfo::SetDeclaration

Imposta la dichiarazione di vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeclaration* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntatore a una matrice [**di elementi D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetDeclaration**](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




