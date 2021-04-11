---
description: Compila una matrice di trasformazione affine 3D. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Funzione D3DXMatrixAffineTransformation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 025485f0015e6f2d85851c8f0919f5462b2bdc3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355439"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a>Funzione D3DXMatrixAffineTransformation (D3dx9math. h)

Compila una matrice di trasformazione affine 3D. Gli argomenti **null** vengono considerati come trasformazioni di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , un punto che identifica il centro della rotazione. Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*protazione* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione. Se questo argomento è **null**, una matrice di identità M <sub>r</sub> viene applicata alla formula nei commenti.

</dd> <dt>

*pTranslation* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta la traduzione. Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.

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

M <sub>r</sub> = matrice di rotazione (*protation*)

Mt = matrice di traslazione (*pTranslation*)

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXMatrixAffineTransformation** può essere utilizzata come parametro per un'altra funzione.

Per le trasformazioni affini 2D, usare [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation**](d3dxmatrixtransformation.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
