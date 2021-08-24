---
description: 'Metodo ID3DXRenderToEnvMap::OnResetDevice: usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.'
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: Metodo ID3DXRenderToEnvMap::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1eb90fd50350fb4cbb21be0ff1cb91972481c57e6752b8ce9b603c86e3b050fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628821"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a>Metodo ID3DXRenderToEnvMap::OnResetDevice

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

**ID3DXRenderToEnvMap::OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9::Reset)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)prima di chiamare qualsiasi altro metodo. Si tratta di un buon punto in cui è possibile acquisire nuovamente le risorse di memoria video e acquisire blocchi di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
