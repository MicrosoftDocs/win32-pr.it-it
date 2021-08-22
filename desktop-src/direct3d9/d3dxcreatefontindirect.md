---
description: Crea un oggetto carattere indirettamente sia per un dispositivo che per un tipo di carattere.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Funzione D3DXCreateFontIndirect (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 555c4b1f3615639d9da01fb7a2a96aa5cb15f697235c918d5130ffcd4d43baa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988661"
---
# <a name="d3dxcreatefontindirect-function"></a>Funzione D3DXCreateFontIndirect

Crea un oggetto carattere indirettamente sia per un dispositivo che per un tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) il dispositivo da associare all'oggetto tipo di carattere.

</dd> <dt>

*pDesc* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***

Puntatore a [**una struttura \_ DESC D3DXFONT,**](d3dxfont-desc.md) che descrive gli attributi dell'oggetto tipo di carattere da creare. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati D3DXFONT DESC viene risolto in D3DXFONT DESCW; in caso contrario, il tipo di dati viene risolto \_ \_ in D3DXFONT \_ DESCA. Vedere la sezione Osservazioni.

</dd> <dt>

*ppFont* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXFONT**](id3dxfont.md)\***

Restituisce un puntatore a [**un'interfaccia ID3DXFont,**](id3dxfont.md) che rappresenta l'oggetto carattere creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXCreateFontIndirectW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontIndirectA perché vengono usate stringhe ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[per utilizzo generico funzioni](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
