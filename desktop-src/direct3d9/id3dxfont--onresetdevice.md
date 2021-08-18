---
description: 'Metodo ID3DXFont::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: Metodo ID3DXFont::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 37e09bab2473ace06b9e0fa803db523453ccff4796693d9faa1d410f5a6630f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748201"
---
# <a name="id3dxfontonresetdevice-method"></a>Metodo ID3DXFont::OnResetDevice

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

**OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), prima che venga chiamato qualsiasi altro metodo. Si tratta di un buon punto per acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
