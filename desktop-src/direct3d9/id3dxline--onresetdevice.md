---
description: 'Metodo ID3DXLine::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: Metodo ID3DXLine::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 349aa7a5b9442076dad64212cca74241238b8c1ad32f890e6e07f84c3256019c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856571"
---
# <a name="id3dxlineonresetdevice-method"></a>Metodo ID3DXLine::OnResetDevice

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

**ID3DXLine::OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato [**(usando IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)prima che venga chiamato qualsiasi altro metodo. Si tratta di un buon punto per acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
