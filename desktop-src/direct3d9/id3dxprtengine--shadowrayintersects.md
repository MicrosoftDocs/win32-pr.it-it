---
description: Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh. Viene in genere utilizzato per determinare se un punto specificato è ombreggiato.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'Metodo ID3DXPRTEngine:: ShadowRayIntersects (D3DX9Mesh. h)'
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
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058629"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>Metodo ID3DXPRTEngine:: ShadowRayIntersects

Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh. Viene in genere utilizzato per determinare se un punto specificato è ombreggiato.

## <a name="syntax"></a>Sintassi


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRayPos* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica il punto in cui inizia il raggio.

</dd> <dt>

*pRayDir* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione normalizzata del raggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Restituisce **true** se il raggio interseca la mesh corrente; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Usare [**ID3DXPRTEngine:: SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) per impostare le distanze minime e massime dell'intersezione con il raggio.

Questo metodo viene eseguito più velocemente di [**ID3DXPRTEngine:: ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
