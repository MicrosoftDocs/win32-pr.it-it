---
description: Ripristina lo stato del dispositivo al momento della chiamata a ID3DXLine::Begin.
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: Metodo ID3DXLine::End (D3dx9core.h)
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
ms.openlocfilehash: 371463bfc24cbdba63ac51c9b729c267b9d020dd260d6d1b6c6a378bb38c3524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987231"
---
# <a name="id3dxlineend-method"></a>Metodo ID3DXLine::End

Ripristina lo stato del dispositivo al momento della [**chiamata a ID3DXLine::Begin.**](id3dxline--begin.md)

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

**ID3DXLine::End** non può essere usato come sostituzione di [**IDirect3DDevice9::EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine::Begin**](id3dxline--begin.md)
</dt> </dl>

 

 




