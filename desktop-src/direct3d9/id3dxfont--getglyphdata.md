---
description: Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: Metodo ID3DXFont::GetGlyphData (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7981e10497dc263a60ae2d5e176fd4d95746b3193d7a5b606aea16afa1188ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629890"
---
# <a name="id3dxfontgetglyphdata-method"></a>Metodo ID3DXFont::GetGlyphData

Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Glifo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore del glifo.

</dd> <dt>

*ppTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Indirizzo di un puntatore a [**un oggetto IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che contiene il glifo.

</dd> <dt>

*pBlackBox* \[ Cambio\]
</dt> <dd>

Tipo: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Puntatore all'oggetto rettangolo più piccolo che racchiude completamente il glifo.

</dd> <dt>

*pCellInc* \[ Cambio\]
</dt> <dd>

Tipo: **[ **POINT**](../winprog/windows-data-types.md)\***

Puntatore al vettore bidimensionale che connette l'origine della cella di caratteri corrente all'origine della cella di caratteri successiva. Vedere [**POINT**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
