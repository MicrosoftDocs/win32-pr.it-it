---
description: Compila una matrice di trasformazione affine 2D nel piano XY. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: Funzione D3DXMatrixAffineTransformation2D (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322506"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a>Funzione D3DXMatrixAffineTransformation2D (D3dx9math. h)

Compila una matrice di trasformazione affine 2D nel piano XY. Gli argomenti **null** vengono considerati come trasformazioni di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Ridimensionamento* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di scala.

</dd> <dt>

*pRotationCenter* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , un punto che identifica il centro della rotazione. Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*Rotazione* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Angolo di rotazione.

</dd> <dt>

*pTranslation* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , che rappresenta la traduzione. Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di trasformazione affine.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:

M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>rc</sub> \* mt

dove:

M <sub>out</sub> = matrice di output (*broncio*)

MS = scala della matrice (*scalabilità*)

M <sub>RC</sub> = matrice Center of rotation (*pRotationCenter*)

M <sub>r</sub> = matrice di rotazione (*rotazione*)

Mt = matrice di traslazione (*pTranslation*)

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXMatrixAffineTransformation2D** può essere utilizzata come parametro per un'altra funzione.

Per le trasformazioni affini 3D, usare [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
