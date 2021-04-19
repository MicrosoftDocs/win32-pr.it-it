---
description: Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: Metodo ID3DX10Font::P reloadGlyphs (D3DX10. h)
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
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322754"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>ID3DX10Font::P metodo reloadGlyphs

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

Non verrà eseguito il rendering dei glifi nel dispositivo. ID3DX10Font: è necessario chiamare:D rawText per eseguire il rendering dei glifi. Tuttavia, se si precaricano i glifi nella memoria video, ID3DX10Font::D rawText utilizzerà in modo sostanziale un minor numero di risorse della CPU.

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

 

 
