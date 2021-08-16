---
description: Calcola il prodotto del punto di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Funzione D3DXPlaneDotCoord (D3dx9math.h)
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
ms.openlocfilehash: 30f04ec310ce66dc43073e724b08c358cd8fc6f24f0b3840475a1abc61544503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524928"
---
# <a name="d3dxplanedotcoord-function"></a>Funzione D3DXPlaneDotCoord

Calcola il prodotto del punto di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia 1.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pP* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore a una [**struttura D3DXPLANE di**](d3dxplane.md) origine.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Prodotto del punto del piano e del vettore 3D.

## <a name="remarks"></a>Commenti

Dato un piano (a, b, c, d) e un vettore 3D (x, y, z), il valore restituito di questa funzione è \* x + b y + c z + d \* \* \* 1. La **funzione D3DXPlaneDotCoord** è utile per determinare la relazione del piano con una coordinata nello spazio 3D.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
