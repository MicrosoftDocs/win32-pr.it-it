---
description: 'Metodo ID3DXSprite::OnLostDevice: usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.'
ms.assetid: 60028f18-21fe-428b-9bee-d5359671da81
title: Metodo ID3DXSprite::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5515945ec8575937a90eb719eca4efd681be5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117779"
---
# <a name="id3dxspriteonlostdevice-method"></a>Metodo ID3DXSprite::OnLostDevice

Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente [**chiami IDirect3DDevice9::Reset.**](/windows/desktop/api) Anche se il dispositivo non è stato effettivamente perso, **ID3DXSprite::OnLostDevice** è responsabile dello sblocco degli blocchi di stato e di altre risorse che potrebbero dover essere rilasciate prima di reimpostare il dispositivo. Di conseguenza, l'oggetto tipo di carattere non può essere usato di nuovo prima di chiamare **IDirect3DDevice9::Reset** e [**quindi ID3DXSprite::OnResetDevice**](id3dxsprite--onresetdevice.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




