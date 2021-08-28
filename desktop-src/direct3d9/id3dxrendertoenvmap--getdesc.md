---
description: Recupera la descrizione della superficie di rendering.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: Metodo ID3DXRenderToEnvMap::GetDesc (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfe9f3e8e857806895ec8be249d51f63ffe4818f24bbbf12d842754a885e855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847306"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a>Metodo ID3DXRenderToEnvMap::GetDesc

Recupera la descrizione della superficie di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***

Puntatore a [**una struttura \_ DESC D3DXRTE**](d3dxrte-desc.md) che descrive la superficie di rendering.

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

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




