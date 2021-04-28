---
description: 'Metodo ID3DXBaseMesh::GetVertexBuffer: recupera il buffer dei vertici associato alla mesh.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: Metodo ID3DXBaseMesh::GetVertexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115369"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a>Metodo ID3DXBaseMesh::GetVertexBuffer

Recupera il buffer dei vertici associato alla mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppVB* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DVertexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) che rappresenta l'oggetto vertex buffer associato alla mesh.

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

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
