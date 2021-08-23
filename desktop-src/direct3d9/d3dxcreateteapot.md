---
description: Usa un sistema di coordinate mancino per creare una mesh contenente una teiera.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: Funzione D3DXCreateTeapot (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d016d69d1b510e504f3cf0b7ec54f69943d1b3db5f16347f8eeaadd75f3f212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988521"
---
# <a name="d3dxcreateteapot-function"></a>Funzione D3DXCreateTeapot

Usa un sistema di coordinate mancino per creare una mesh contenente una teiera.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato alla mesh di teiera creata.

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore alla forma di output, [**un'interfaccia ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*ppAdjacency* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Quando il metodo viene restituito, questo parametro viene riempito con una matrice di tre DWORD per ogni viso che specificano i tre elementi adiacenti per ogni viso nella mesh. È possibile specificare **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione crea una mesh con l'opzione di creazione gestita D3DXMESH e \_ [D3DFVF \_ XYZ \| D3DFVF \_ NORMAL](d3dfvf.md) flexible vertex format (FVF).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di disegno delle forme](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
