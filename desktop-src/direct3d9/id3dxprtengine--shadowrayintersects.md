---
description: Usa il ray tracing efficiente nelle simulazioni PRT (Precomputed Radiance Transfer) per determinare se un raggio interseca una mesh. Utilizzato in genere per determinare se un determinato punto è ombreggiato.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: Metodo ID3DXPRTEngine::ShadowRayIntersects (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5064e788d89de6e5143ad826a4f61a4afd802931c6964193c8fa46626edf955d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729595"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>Metodo ID3DXPRTEngine::ShadowRayIntersects

Usa il ray tracing efficiente nelle simulazioni PRT (Precomputed Radiance Transfer) per determinare se un raggio interseca una mesh. Utilizzato in genere per determinare se un determinato punto è ombreggiato.

## <a name="syntax"></a>Sintassi


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRayPos* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la direzione normalizzata del raggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Restituisce **TRUE** se il raggio interseca la mesh corrente. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

Usare [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) per impostare le distanze minime e massime di intersezione con il raggio.

Questo metodo viene eseguito più velocemente rispetto a [**ID3DXPRTEngine::ClosestRayIntersects.**](id3dxprtengine--closestrayintersects.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
