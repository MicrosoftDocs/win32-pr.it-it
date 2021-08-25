---
description: 'Funzione D3DXPlaneNormalize (D3dx9math.h): normalizza i coefficienti del piano in modo che la normale del piano abbia lunghezza unità.'
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Funzione D3DXPlaneNormalize (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a8a5a80526e013c85caf59b3a6a3d6c595a3c10a6e29687882c7789765368d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952311"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>Funzione D3DXPlaneNormalize (D3dx9math.h)

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

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore alla [**struttura D3DXPLANE**](d3dxplane.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pP* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore alla struttura [**D3DXPLANE di**](d3dxplane.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore a [**una struttura D3DXPLANE**](d3dxplane.md) che rappresenta la normale del piano.

## <a name="remarks"></a>Commenti

Questa funzione normalizza un piano in modo che \| a,b,c \| == 1.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, questa funzione può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




