---
description: 'Ripristina lo stato del dispositivo nel modo in cui si trovava quando è stato chiamato ID3DXLine:: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'Metodo ID3DXLine:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323473"
---
# <a name="id3dxlineend-method"></a>Metodo ID3DXLine:: end

Ripristina lo stato del dispositivo nel modo in cui si trovava quando è stato chiamato [**ID3DXLine:: Begin**](id3dxline--begin.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT End();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Non è possibile usare **ID3DXLine:: end** come sostituto di [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine:: Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




