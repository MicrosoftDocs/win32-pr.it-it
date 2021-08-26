---
description: Crea un oggetto sprite associato a un particolare dispositivo. Gli oggetti Sprite vengono usati per disegnare immagini 2D sullo schermo.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Funzione D3DXCreateSprite (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fe6d4897a581302f27544217c3caf5b6c723ce2ff4aed611b40a21cd7b0d35f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027741"
---
# <a name="d3dxcreatesprite-function"></a>Funzione D3DXCreateSprite

Crea un oggetto sprite associato a un particolare dispositivo. Gli oggetti Sprite vengono usati per disegnare immagini 2D sullo schermo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) il dispositivo da associare allo sprite.

</dd> <dt>

*ppSprite* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXSprite.**](id3dxsprite.md) Questa interfaccia consente all'utente di accedere alle funzioni sprite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è S \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa interfaccia può essere usata per disegnare immagini bidimensionali nello spazio dello schermo del dispositivo associato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
