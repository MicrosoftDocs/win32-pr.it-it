---
description: Calcola il prodotto a punti di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Funzione D3DXPlaneDotNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322101"
---
# <a name="d3dxplanedotnormal-function"></a>D3DXPlaneDotNormal (funzione)

Calcola il prodotto a punti di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia 0.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXPlaneDotNormal(
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

Dato un piano (a, b, c, d) e un vettore 3D (x, y, z), il valore restituito di questa funzione è \* x + b \* y + c \* z + d \* 0. La funzione **D3DXPlaneDotNormal** è utile per calcolare l'angolo tra la normale del piano e un altro normale.

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

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> </dl>

 

 
