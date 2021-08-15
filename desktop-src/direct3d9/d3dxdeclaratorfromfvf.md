---
description: Restituisce un dichiaratore da un codice FVF (Flexible Vertex Format).
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: Funzione D3DXDeclaratorFromFVF (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd7122ccad0e2f12821892c49a08348ffd6cd9d171cc652e5f2f05853fe61e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526183"
---
# <a name="d3dxdeclaratorfromfvf-function"></a>Funzione D3DXDeclaratorFromFVF

Restituisce un dichiaratore da un codice FVF (Flexible Vertex Format).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FVF* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione [di D3DFVF](d3dfvf.md) che descrive il file FVF da cui generare la matrice del dichiaratore restituita.

</dd> <dt>

*Dichiarazione* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrivono il formato dei vertici della mesh. Il limite superiore di questa matrice di dichiaratori è [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXERR \_ INVALIDMESH.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
