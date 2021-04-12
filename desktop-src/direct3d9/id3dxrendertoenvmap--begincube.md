---
description: Avviare il rendering di una mappa dell'ambiente cubica.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'Metodo ID3DXRenderToEnvMap:: BeginCube (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bff6c8f3bdc49dfe0c1b677c6805cb332c05007d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354574"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a>Metodo ID3DXRenderToEnvMap:: BeginCube

Avviare il rendering di una mappa dell'ambiente cubica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCubeTex* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) che rappresenta la trama del cubo a cui eseguire il rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Per creare ognuno dei 6 visi, vedere [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .

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

 

 
