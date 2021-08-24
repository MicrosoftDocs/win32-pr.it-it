---
description: Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: Metodo ID3DXFont::P reloadGlyphs (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea422a6e0b0ecfda6b4eb03a0636eb013d8c840c96cec6f1c482589de29f3c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563931"
---
# <a name="id3dxfontpreloadglyphs-method"></a>Metodo ID3DXFont::P reloadGlyphs

Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prima di tutto* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

ID del primo glifo da caricare nella memoria video.

</dd> <dt>

*Ultimo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

ID dell'ultimo glifo da caricare nella memoria video.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Questo metodo genera trame che contengono i glifi di input. I glifi vengono disegnati come una serie di triangoli.

Non verrà eseguito il rendering dei glifi nel dispositivo. [**DrawText**](id3dxfont--drawtext.md) deve comunque essere chiamato per eseguire il rendering dei glifi. Tuttavia, precaricando i glifi nella memoria video, **DrawText** userà sostanzialmente meno risorse DELLA CPU.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
