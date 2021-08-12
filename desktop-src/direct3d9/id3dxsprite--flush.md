---
description: Forza l'invio di tutti gli sprite in batch al dispositivo. Gli stati del dispositivo rimangono invariati dopo l'ultima chiamata a ID3DXSprite::Begin. L'elenco degli sprite in batch viene quindi cancellato.
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: Metodo ID3DXSprite::Flush (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 766fbe41491fc6861ac3eaf366c3a858870c560139f1048d405184b580e72229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292693"
---
# <a name="id3dxspriteflush-method"></a>Metodo ID3DXSprite::Flush

Forza l'invio di tutti gli sprite in batch al dispositivo. Gli stati del dispositivo rimangono invariati dopo l'ultima chiamata a [**ID3DXSprite::Begin.**](id3dxsprite--begin.md) L'elenco degli sprite in batch viene quindi cancellato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::End**](id3dxsprite--end.md)
</dt> </dl>

 

 




