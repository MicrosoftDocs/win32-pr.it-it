---
description: Avviare il rendering di una mappa dell'ambiente parabolica.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'Metodo ID3DXRenderToEnvMap:: BeginParabolic (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058596"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a>Metodo ID3DXRenderToEnvMap:: BeginParabolic

Avviare il rendering di una mappa dell'ambiente parabolica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexZPos* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama di rendering positiva.

</dd> <dt>

*pTexZNeg* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama di rendering negativa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL. E \_ non riescono

## <a name="remarks"></a>Commenti

Per creare le facce, vedere [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: end**](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
