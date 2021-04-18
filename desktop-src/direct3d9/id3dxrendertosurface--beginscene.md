---
description: Inizia una scena.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'Metodo ID3DXRenderToSurface:: BeginScene (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323527"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a>Metodo ID3DXRenderToSurface:: BeginScene

Inizia una scena.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSurface* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , che rappresenta la superficie di rendering.

</dd> <dt>

*pViewport* \[ in\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Puntatore a una struttura [**D3DVIEWPORT9**](d3dviewport9.md) che descrive il viewport per la scena.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL. D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ INVALIDDATA E \_ OutOfMemory

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
