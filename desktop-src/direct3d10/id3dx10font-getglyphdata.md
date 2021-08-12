---
description: Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: Metodo ID3DX10Font::GetGlyphData (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eaabcd6de2acf5ec86ab8c9a47d4224ed230104fe189816abd9d02fd3ac09596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302891"
---
# <a name="id3dx10fontgetglyphdata-method"></a>Metodo ID3DX10Font::GetGlyphData

Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
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

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Indirizzo di un puntatore a un oggetto ID3D10Texture che contiene il glifo.

</dd> <dt>

*pBlackBox* \[ Pollici\]
</dt> <dd>

Tipo: **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***

Puntatore all'oggetto rettangolo più piccolo che racchiude completamente il glifo. Vedere [RECT.](/previous-versions//ms536136(v=vs.85))

</dd> <dt>

*pCellInc* \[ Pollici\]
</dt> <dd>

Tipo: **\* POINT**

Puntatore al vettore bidimensionale che connette l'origine della cella di caratteri corrente all'origine della cella di caratteri successiva. Vedere [POINT](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
