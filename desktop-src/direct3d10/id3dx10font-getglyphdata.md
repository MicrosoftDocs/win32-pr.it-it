---
description: Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'Metodo ID3DX10Font:: GetGlyphData (D3DX10. h)'
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
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323163"
---
# <a name="id3dx10fontgetglyphdata-method"></a>Metodo ID3DX10Font:: GetGlyphData

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

*Glifo* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore glifo.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Indirizzo di un puntatore a un oggetto ID3D10Texture che contiene il glifo.

</dd> <dt>

*pBlackBox* \[ in\]
</dt> <dd>

Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Puntatore all'oggetto rettangolo più piccolo che racchiude completamente il glifo. Vedere [Rect](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*pCellInc* \[ in\]
</dt> <dd>

Tipo: **punto \***

Puntatore al vettore bidimensionale che connette l'origine della cella del carattere corrente all'origine della cella di caratteri successiva. Vedere [punto](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
