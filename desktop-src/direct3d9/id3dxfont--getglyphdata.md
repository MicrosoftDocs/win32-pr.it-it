---
description: Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'Metodo ID3DXFont:: GetGlyphData (D3dx9core. h)'
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
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322617"
---
# <a name="id3dxfontgetglyphdata-method"></a>Metodo ID3DXFont:: GetGlyphData

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

*Glifo* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore glifo.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Indirizzo di un puntatore a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che contiene il glifo.

</dd> <dt>

*pBlackBox* \[ out\]
</dt> <dd>

Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Puntatore all'oggetto rettangolo più piccolo che racchiude completamente il glifo.

</dd> <dt>

*pCellInc* \[ out\]
</dt> <dd>

Tipo: **[ **punto**](../winprog/windows-data-types.md)\***

Puntatore al vettore bidimensionale che connette l'origine della cella del carattere corrente all'origine della cella di caratteri successiva. Vedere [**punto**](../winprog/windows-data-types.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
