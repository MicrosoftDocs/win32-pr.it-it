---
description: Recupera i parametri della superficie di rendering.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: Metodo ID3DXRenderToSurface::GetDesc (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7dd6787ad8a81491e92af2a5ec1a16253af4cd0a0f8cb075dde01461b0010d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790481"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>Metodo ID3DXRenderToSurface::GetDesc

Recupera i parametri della superficie di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pParameters* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***

Puntatore a [**una struttura \_ DESC D3DXRTS,**](d3dxrts-desc.md) che descrive i parametri della superficie di rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




