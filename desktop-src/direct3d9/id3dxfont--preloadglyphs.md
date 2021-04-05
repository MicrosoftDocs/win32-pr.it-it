---
description: Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: Metodo ID3DXFont::P reloadGlyphs (D3dx9core. h)
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
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058684"
---
# <a name="id3dxfontpreloadglyphs-method"></a>ID3DXFont::P metodo reloadGlyphs

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

*Primo* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID del primo glifo da caricare nella memoria video.

</dd> <dt>

*Ultima* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID dell'ultimo glifo da caricare nella memoria video.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Questo metodo genera trame che contengono i glifi di input. I glifi vengono disegnati come una serie di triangoli.

Non verrà eseguito il rendering dei glifi nel dispositivo. Per eseguire il rendering dei glifi, è comunque necessario chiamare [**DrawText**](id3dxfont--drawtext.md) . Tuttavia, se si precaricano i glifi nella memoria video, **DrawText** utilizzerà in modo sostanziale un minor numero di risorse della CPU.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
