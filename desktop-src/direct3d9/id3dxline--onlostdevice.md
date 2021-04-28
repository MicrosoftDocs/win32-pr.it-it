---
description: 'Metodo ID3DXLine::OnLostDevice: usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.'
ms.assetid: a5c82a58-10f9-44bd-a42f-555867b2c857
title: Metodo ID3DXLine::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f3845e40e4ece115704c38904a61dbca3c24443
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093679"
---
# <a name="id3dxlineonlostdevice-method"></a>Metodo ID3DXLine::OnLostDevice

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

Questo metodo deve essere chiamato ogni volta che il dispositivo viene perso o prima che l'utente [**chiami IDirect3DDevice9::Reset.**](/windows/desktop/api) Anche se il dispositivo non è stato effettivamente perso, **ID3DXLine::OnLostDevice** è responsabile del rilascio di blocchi di stato e di altre risorse che potrebbero essere necessarie per essere rilasciate prima di reimpostare il dispositivo. Di conseguenza, l'oggetto tipo di carattere non può essere usato di nuovo prima di chiamare **IDirect3DDevice9::Reset** e [**quindi ID3DXLine::OnResetDevice**](id3dxline--onresetdevice.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 




