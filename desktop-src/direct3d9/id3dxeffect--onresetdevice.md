---
description: 'Metodo ID3DXEffect::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: Metodo ID3DXEffect::OnResetDevice (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9c48d93bc5ebf6aa10816f384090da871188220c8b7d0ed17b1f042f292e9024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121514"
---
# <a name="id3dxeffectonresetdevice-method"></a>Metodo ID3DXEffect::OnResetDevice

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

**ID3DXEffect::OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato [**(usando IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)prima che venga chiamato qualsiasi altro metodo. Si tratta di un buon punto per acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
