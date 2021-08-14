---
description: Restituisce un codice FVF (Flexible Vertex Format) da un dichiaratore.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: Funzione D3DXFVFFromDeclarator (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f9bad9968a52fb6c3b11de96936f48e432bd038e172318cb52f21fad4b08ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525648"
---
# <a name="d3dxfvffromdeclarator-function"></a>Funzione D3DXFVFFromDeclarator

Restituisce un codice FVF (Flexible Vertex Format) da un dichiaratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeclaration* \[ Pollici\]
</dt> <dd>

Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrivono il codice FVF.

</dd> <dt>

*pFVF* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a un valore DWORD, che rappresenta la combinazione restituita di [D3DFVF](d3dfvf.md) che descrive il formato dei vertici restituito dal dichiaratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questa funzione avrà esito negativo per qualsiasi dichiaratore che non esegue il mapping direttamente a un FVF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
