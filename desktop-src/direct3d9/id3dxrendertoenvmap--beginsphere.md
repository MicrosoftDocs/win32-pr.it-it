---
description: Avviare il rendering di una mappa dell'ambiente sferico.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: Metodo ID3DXRenderToEnvMap::BeginSphere (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f8bc555e3ea4f4fbb895c42f5c7a407cea88aedeacb9604ad1e78c7003bdf34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801291"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a>Metodo ID3DXRenderToEnvMap::BeginSphere

Avviare il rendering di una mappa dell'ambiente sferico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a [**un'interfaccia IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama di cui eseguire il rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL. E \_ FAIL

## <a name="remarks"></a>Commenti

Vedere [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) per disegnare il viso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap::End**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
