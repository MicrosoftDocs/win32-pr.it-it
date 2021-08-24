---
description: 'Funzione D3DXPlaneNormalize (D3DX10Math.h): normalizza i coefficienti del piano in modo che la normale del piano abbia lunghezza unità.'
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Funzione D3DXPlaneNormalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf4429e324a5ce1554c5c37c929625153c74764cb9d03618f633f35ecd416748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754151"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a>Funzione D3DXPlaneNormalize (D3DX10Math.h)

Normalizza i coefficienti del piano in modo che la normale del piano abbia lunghezza unità.

## <a name="syntax"></a>Sintassi


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntatore [**all'oggetto D3DXPLANE**](d3d10-d3dxplane.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pP* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntatore alla struttura D3DXPLANE di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntatore a una struttura D3DXPLANE che rappresenta la normale del piano.

## <a name="remarks"></a>Commenti

Questa funzione normalizza un piano in modo che \| a,b,c \| == 1.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, questa funzione può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
