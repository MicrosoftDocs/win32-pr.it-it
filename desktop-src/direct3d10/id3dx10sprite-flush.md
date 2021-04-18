---
description: "Forzare l'invio di tutti gli sprite in batch al dispositivo. Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a ID3DX10Sprite:: Begin. L'elenco degli sprite in batch viene quindi cancellato."
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'Metodo ID3DX10Sprite:: Flush (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323744"
---
# <a name="id3dx10spriteflush-method"></a>Metodo ID3DX10Sprite:: Flush

Forzare l'invio di tutti gli sprite in batch al dispositivo. Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a ID3DX10Sprite:: Begin. L'elenco degli sprite in batch viene quindi cancellato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Flush();
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

 

 




