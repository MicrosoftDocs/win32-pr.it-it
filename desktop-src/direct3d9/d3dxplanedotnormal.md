---
description: Calcola il prodotto del punto di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Funzione D3DXPlaneDotNormal (D3dx9math.h)
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
ms.openlocfilehash: 95259cd880d22678ef91765d38c68e85f5f0443ac7058de4b3a2dd078d7ad55a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910518"
---
# <a name="d3dxplanedotnormal-function"></a>Funzione D3DXPlaneDotNormal

Calcola il prodotto del punto di un piano e di un vettore 3D. Si presuppone che il parametro w del vettore sia 0.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXPlaneDotNormal(
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

Dato un piano (a, b, c, d) e un vettore 3D (x, y, z) il valore restituito di questa funzione è \* x + b y + c z + d \* \* \* 0. La **funzione D3DXPlaneDotNormal** è utile per calcolare l'angolo tra la normale del piano e un'altra normale.

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

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> </dl>

 

 
