---
description: Chiamare questo metodo dopo ID3DX10Sprite::Flush. Se al momento della chiamata a ID3DX10Sprite::Begin è stato specificato D3DX10 SPRITE SAVE STATE, questa API ripristina lo stato del dispositivo allo stato precedente alla chiamata di \_ \_ \_ ID3DX10Sprite::Begin.
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: Metodo ID3DX10Sprite::End (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02cfa1e92275230bd3a853aa9079187181089c46b4e4f193404b9dc0c709c9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302290"
---
# <a name="id3dx10spriteend-method"></a>Metodo ID3DX10Sprite::End

Chiamare questo metodo dopo ID3DX10Sprite::Flush. Se al momento della chiamata a ID3DX10Sprite::Begin è stato specificato D3DX10 SPRITE SAVE STATE, questa API ripristina lo stato del dispositivo allo stato precedente alla chiamata di \_ \_ \_ ID3DX10Sprite::Begin.

## <a name="syntax"></a>Sintassi


```C++
HRESULT End();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




