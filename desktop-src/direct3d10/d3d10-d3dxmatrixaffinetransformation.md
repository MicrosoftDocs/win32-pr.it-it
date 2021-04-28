---
description: 'Funzione D3DXMatrixAffineTransformation (D3DX10Math.h): compila una matrice di trasformazione affine 3D. Gli argomenti NULL vengono considerati trasformazioni di identità.'
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Funzione D3DXMatrixAffineTransformation (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01c6b3c3ffe2de9b7c7003b78f1b07a0f35cc3a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113179"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>Funzione D3DXMatrixAffineTransformation (D3DX10Math.h)

Compila una matrice di trasformazione affine 3D. **Gli** argomenti NULL vengono considerati trasformazioni di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore [**all'oggetto D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*Ridimensionamento* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di scala.

</dd> <dt>

*pRotationCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a [**un oggetto D3DXVECTOR3,**](d3d10-d3dxvector3.md)un punto che identifica il centro di rotazione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>rc.</sub>

</dd> <dt>

*pRotation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore a [**un oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che specifica la rotazione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>r.</sub>

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 che rappresenta la traslazione. Se questo argomento è **NULL,** viene applicata una matrice Identity Mt alla formula in Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX che è una matrice di trasformazione affine.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con la concatenazione di matrici valutata in ordine da sinistra a destra:

M<sub>out</sub> = Ms \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

dove:

M<sub>out</sub> = matrice di output (pOut)

Ms = matrice di ridimensionamento (ridimensionamento)

M<sub>rc</sub> = centro della matrice di rotazione (pRotationCenter)

M<sub>r</sub> = matrice di rotazione (pRotation)

Mt = matrice di traslazione (pTranslation)

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixAffineTransformation può essere usata come parametro per un'altra funzione.

Per le trasformazioni affine 2D, usare D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
