---
description: Avviare il rendering di una mappa dell'ambiente emisferico.
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: Metodo ID3DXRenderToEnvMap::BeginHemisphere (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa3aaa9abff51abc88042c87a0663011775c920097febefa9c3582c4db55636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674771"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a>Metodo ID3DXRenderToEnvMap::BeginHemisphere

Avviare il rendering di una mappa dell'ambiente emisferico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexZPos* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a [**un'interfaccia IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la superficie di rendering della trama positiva.

</dd> <dt>

*pTexZNeg* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntatore a [**un'interfaccia IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la superficie di rendering negativa della trama.

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

 

 
