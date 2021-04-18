---
description: 'Chiamare questo dopo ID3DX10Sprite:: Flush. Se è \_ stato \_ \_ specificato lo stato d3dx10 sprite Save quando ID3DX10Sprite:: Begin è stato chiamato, questa API ripristinerà lo stato del dispositivo come prima della chiamata a ID3DX10Sprite:: Begin.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'Metodo ID3DX10Sprite:: end (D3DX10. h)'
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
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323745"
---
# <a name="id3dx10spriteend-method"></a>Metodo ID3DX10Sprite:: end

Chiamare questo dopo ID3DX10Sprite:: Flush. Se è \_ stato \_ \_ specificato lo stato d3dx10 sprite Save quando ID3DX10Sprite:: Begin è stato chiamato, questa API ripristinerà lo stato del dispositivo come prima della chiamata a ID3DX10Sprite:: Begin.

## <a name="syntax"></a>Sintassi


```C++
HRESULT End();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

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

 

 




