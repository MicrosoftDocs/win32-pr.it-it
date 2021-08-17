---
description: 'Metodo ID3DXSprite::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: 74f8616e-c3ed-4231-b701-009213ea48c0
title: Metodo ID3DXSprite::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16086aca86e0df8c2c75e6a055be9fa95f7cc97259f37401aa932af962409811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800579"
---
# <a name="id3dxspriteonresetdevice-method"></a>Metodo ID3DXSprite::OnResetDevice

Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

**ID3DXSprite::OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)prima che venga chiamato qualsiasi altro metodo. Si tratta di un buon punto per acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 
