---
description: Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: Metodo ID3DX10Font::P reloadGlyphs (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 358523135db83f2ec7f973fce403a44d2f0ece82ab60cf9527cb612ccde61e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540337"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>Metodo ID3DX10Font::P reloadGlyphs

Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*First (Prima)* \[ Pollici\]
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

Non verrà eseguito il rendering dei glifi nel dispositivo. ID3DX10Font::D rawText deve comunque essere chiamato per eseguire il rendering dei glifi. Tuttavia, precaricando i glifi nella memoria video, ID3DX10Font::D rawText userà notevolmente meno risorse della CPU.

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

 

 
