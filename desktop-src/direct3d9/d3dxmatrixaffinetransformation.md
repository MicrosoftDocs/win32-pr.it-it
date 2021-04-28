---
description: 'Funzione D3DXMatrixAffineTransformation (D3dx9math.h): compila una matrice di trasformazione affine 3D. Gli argomenti NULL vengono trattati come trasformazioni di identità.'
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Funzione D3DXMatrixAffineTransformation (D3dx9math.h)
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
ms.openlocfilehash: 7329ffbffe5ffd89ed64e5386246f39699618960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094169"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a>Funzione D3DXMatrixAffineTransformation (D3dx9math.h)

Compila una matrice di trasformazione affine 3D. **Gli** argomenti NULL vengono trattati come trasformazioni di identità.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Ridimensionamento* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di scala.

</dd> <dt>

*pRotationCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) un punto che identifica il centro di rotazione. Se questo argomento è **NULL,** una matrice identity M <sub>rc</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*pRotation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione. Se questo argomento è **NULL,** una matrice di identità M <sub>r</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta la traslazione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Mt.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che è una matrice di trasformazione affine.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con la concatenazione di matrici valutata in ordine da sinistra a destra:

M<sub>out</sub> = Ms \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

dove:

M <sub>out</sub> = matrice di output (*pOut*)

Ms = matrice di ridimensionamento (*ridimensionamento*)

M <sub>rc</sub> = centro della matrice di rotazione (*pRotationCenter*)

M <sub>r</sub> = matrice di rotazione (*pRotation*)

Mt = matrice di conversione (*pTranslation*)

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXMatrixAffineTransformation** può essere usata come parametro per un'altra funzione.

Per le trasformazioni affine 2D, usare [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixTransformation**](d3dxmatrixtransformation.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
