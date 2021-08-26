---
description: Compila una matrice di trasformazione affine 2D nel piano x-y. Gli argomenti NULL vengono trattati come trasformazioni di identità.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: Funzione D3DXMatrixAffineTransformation2D (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 40666e4fc74f834d6333259636f9953281d534570eedabf37a3d99590ec2e1ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070161"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a>Funzione D3DXMatrixAffineTransformation2D (D3DX10Math.h)

Compila una matrice di trasformazione affine 2D nel piano x-y. **Gli** argomenti NULL vengono trattati come trasformazioni di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
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

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a [**un oggetto D3DXVECTOR2,**](d3d10-d3dxvector2.md)un punto che identifica il centro di rotazione. Se questo argomento è **NULL,** una matrice identity M <sub>rc</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*Rotazione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Angolo di rotazione.

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a [**un oggetto D3DXVECTOR2**](d3d10-d3dxvector2.md)che rappresenta la traslazione. Se questo argomento è **NULL,** viene applicata una matrice Identity Mt alla formula in Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX che è una matrice di trasformazione affine.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione affine con la formula seguente, con la concatenazione di matrici valutata nell'ordine da sinistra a destra:

M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ

dove:

M<sub>out</sub> = matrice di output (pOut)

Ms = matrice di ridimensionamento (ridimensionamento)

M<sub>rc</sub> = centro della matrice di rotazione (pRotationCenter)

M<sub>r</sub> = matrice di rotazione (rotazione)

Mt = matrice di traslazione (pTranslation)

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixAffineTransformation2D può essere usata come parametro per un'altra funzione.

Per le trasformazioni affine 3D, usare D3DXMatrixAffineTransformation.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
