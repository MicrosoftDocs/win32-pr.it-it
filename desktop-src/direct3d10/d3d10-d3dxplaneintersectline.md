---
description: "Funzione D3DXPlaneIntersectLine (D3DX10Math.h): trova l'intersezione tra un piano e una linea."
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Funzione D3DXPlaneIntersectLine (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9d70f588c9f4ec54fd5889f8effb503c62235441fe425d38ea9dbed620fd3e8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754161"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a>Funzione D3DXPlaneIntersectLine (D3DX10Math.h)

Trova l'intersezione tra un piano e una linea.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a [**un oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md)che identifica l'intersezione tra il piano e la linea specificati.

</dd> <dt>

*pP* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntatore all'oggetto [**D3DXPLANE di origine.**](d3d10-d3dxplane.md)

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 di origine, che definisce un punto iniziale della riga.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 di origine, che definisce un punto finale di riga.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a una struttura D3DXVECTOR3 che rappresenta l'intersezione tra il piano e la linea specificati.

## <a name="remarks"></a>Commenti

Se la linea è parallela al piano, **viene restituito NULL.**

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXPlaneIntersectLine può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
