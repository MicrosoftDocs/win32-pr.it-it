---
description: Recuperare il dispositivo Direct3D associato all'oggetto tipo di carattere.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: Metodo ID3DX10Font::GetDevice (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0abed8fcb2e5c85b64c58f66f7584d1c6af5f5b6b4ed9e2efd7266ea38a5a8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100406"
---
# <a name="id3dx10fontgetdevice-method"></a>Metodo ID3DX10Font::GetDevice

Recuperare il dispositivo Direct3D associato all'oggetto tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDevice* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Indirizzo di un puntatore a un'interfaccia ID3D10Device, che rappresenta l'oggetto dispositivo Direct3D associato all'oggetto tipo di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

> [!Note]  
> La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni sull'interfaccia ID3D10Device. Assicurarsi di chiamare IUnknown al termine dell'uso di questa interfaccia ID3D10Device o si avrà una perdita di memoria.

 

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

 

 




