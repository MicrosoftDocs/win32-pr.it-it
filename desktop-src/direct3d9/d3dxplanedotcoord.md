---
description: Calcola il prodotto a punti di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia pari a 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Funzione D3DXPlaneDotCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234938"
---
# <a name="d3dxplanedotcoord-function"></a>D3DXPlaneDotCoord (funzione)

Calcola il prodotto a punti di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia pari a 1.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PP* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) di origine.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Prodotto a virgola del piano e del vettore 3D.

## <a name="remarks"></a>Commenti

Dato un piano (a, b, c, d) e un vettore 3D (x, y, z), il valore restituito di questa funzione è \* x + b \* y + c \* z + d \* 1. La funzione **D3DXPlaneDotCoord** è utile per determinare la relazione del piano con una coordinata nello spazio 3D.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
