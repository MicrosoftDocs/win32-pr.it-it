---
description: Recupera il dispositivo Direct3D associato alla superficie di rendering.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: Metodo ID3DXRenderToSurface::GetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7b8ea6887eb1b18b1e2eb28a811f05f10e9df4614ddb8dbc02371acc176c866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729605"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a>Metodo ID3DXRenderToSurface::GetDevice

Recupera il dispositivo Direct3D associato alla superficie di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDevice* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta l'oggetto dispositivo Direct3D associato alla superficie di rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL. La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni [**nell'interfaccia IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'uso di questa **interfaccia IDirect3DDevice9** oppure si verifica una perdita di memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 
