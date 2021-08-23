---
description: Calcola il prodotto del punto di un piano e di un vettore 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Funzione D3DXPlaneDot (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4895a94ad50171682a8bd5247694c3b35a56d174b5477f5bbb2a621c1e74fa96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564631"
---
# <a name="d3dxplanedot-function"></a>Funzione D3DXPlaneDot

Calcola il prodotto del punto di un piano e di un vettore 4D.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
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

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore a [**una struttura D3DXVECTOR4.**](d3dxvector4.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Prodotto del punto del piano e vettore 4D.

## <a name="remarks"></a>Commenti

Dato un piano (a, b, c, d) e un vettore 4D (x, y, z, w) il valore restituito di questa funzione è \* x + b y + c z + d \* \* \* w. La **funzione D3DXPlaneDot** è utile per determinare la relazione del piano con una coordinata omogenea. Ad esempio, questa funzione può essere usata per determinare se una determinata coordinata si trova su un piano specifico o su quale lato di un particolare piano si trova una coordinata specifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
