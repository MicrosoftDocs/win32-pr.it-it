---
description: "Funzione D3DXPlaneIntersectLine (D3dx9math.h): trova l'intersezione tra un piano e una linea."
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: Funzione D3DXPlaneIntersectLine (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1b6f3067b25561869f61c70792ed2a242404deca4d65f07d83e331f6f4414d8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096125"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a>Funzione D3DXPlaneIntersectLine (D3dx9math.h)

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

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che identifica l'intersezione tra il piano e la linea specificati.

</dd> <dt>

*pP* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore alla struttura [**D3DXPLANE di**](d3dxplane.md) origine.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine, che definisce un punto iniziale della riga.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3 di**](d3dxvector3.md) origine, che definisce un punto finale di riga.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a una [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta l'intersezione tra il piano e la linea specificati.

## <a name="remarks"></a>Commenti

Se la linea è parallela al piano, **viene restituito NULL.**

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXPlaneIntersectLine** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




