---
description: Normalizza i coefficienti del piano in modo che la normale del piano abbia la lunghezza dell'unità.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Funzione D3DXPlaneNormalize (D3dx9math. h)
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
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322098"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>Funzione D3DXPlaneNormalize (D3dx9math. h)

Normalizza i coefficienti del piano in modo che la normale del piano abbia la lunghezza dell'unità.

## <a name="syntax"></a>Sintassi


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta la normale del piano.

## <a name="remarks"></a>Commenti

Questa funzione normalizza un piano in modo che \| a, b, c \| = = 1.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, questa funzione può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




