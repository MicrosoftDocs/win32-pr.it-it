---
description: Recupera il dispositivo Direct3D associato all'oggetto tipo di carattere.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: Metodo ID3DXFont::GetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e0f89594f77044db20bade062b245ccabe072a0ccae1fb5fa76f23bb18a8db0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121148"
---
# <a name="id3dxfontgetdevice-method"></a>Metodo ID3DXFont::GetDevice

Recupera il dispositivo Direct3D associato all'oggetto tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDevice* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta l'oggetto dispositivo Direct3D associato all'oggetto tipo di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

> [!Note]  
> La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni [**nell'interfaccia IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'uso di questa **interfaccia IDirect3DDevice9** o si avrà una perdita di memoria.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
