---
description: Preparare un dispositivo per il disegno degli sprite.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'Metodo ID3DX10Sprite:: begin (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235110"
---
# <a name="id3dx10spritebegin-method"></a>Metodo ID3DX10Sprite:: Begin

Preparare un dispositivo per il disegno degli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Flag che controllano il modo in cui verranno disegnati gli sprite. Vedere [**d3dx10 \_ sprite \_ flag**](d3dx10-sprite-flag.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Ogni chiamata a Begin deve corrispondere a una chiamata a [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
