---
description: Recupera i parametri della superficie di rendering.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'Metodo ID3DXRenderToSurface:: getdesc (D3dx9core. h)'
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
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235192"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>Metodo ID3DXRenderToSurface:: getdesc

Recupera i parametri della superficie di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pParameters* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXRTS \_ desc**](d3dxrts-desc.md)\***

Puntatore a una struttura [**D3DXRTS \_ desc**](d3dxrts-desc.md) , che descrive i parametri della superficie di rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




