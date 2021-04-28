---
description: 'Funzione D3DXMatrixTransformation2D (D3DX10Math.h): compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano xy. Gli argomenti NULL vengono considerati trasformazioni di identità.'
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Funzione D3DXMatrixTransformation2D (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ef112c346fd222f5e25935740e47ab62273628f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103359"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>Funzione D3DXMatrixTransformation2D (D3DX10Math.h)

Compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano xy. **Gli** argomenti NULL vengono considerati trasformazioni di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che contiene il risultato delle trasformazioni.

</dd> <dt>

*pScalingCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a [**un oggetto D3DXVECTOR2,**](d3d10-d3dxvector2.md)un punto che identifica il centro di ridimensionamento. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>sc.</sub>

</dd> <dt>

*ScalingRotation* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Puntatore al fattore di rotazione di ridimensionamento.

</dd> <dt>

*pScaling* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2, un punto che identifica la scala. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Ms.

</dd> <dt>

*pRotationCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2, un punto che identifica il centro di rotazione. Se questo argomento è **NULL,** una matrice identity M <sub>rc</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*Rotazione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Angolo di rotazione in radianti.

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 che identifica la traslazione. Se questo argomento è **NULL,** viene applicata una matrice Identity Mt alla formula in Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX che contiene la matrice di trasformazione.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione con la formula seguente, con la concatenazione di matrici valutata nell'ordine da sinistra a destra:

M<sub>out</sub> = (M<sub>sc</sub>)⁻ più \* (M<sub>sr</sub>)⁻ ms \* M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻⁻ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

dove:

M<sub>out</sub> = matrice di output (pOut)

M<sub>sc</sub> = matrice del centro di ridimensionamento (pScalingCenter)

M<sub>sr</sub> = matrice di rotazione di ridimensionamento (pScalingRotation)

Ms = matrice di ridimensionamento (pScaling)

M<sub>rc</sub> = centro della matrice di rotazione (pRotationCenter)

M<sub>r</sub> = matrice di rotazione (rotazione)

Mt = matrice di conversione (pTranslation)

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixTransformation2D può essere usata come parametro per un'altra funzione.

Per le trasformazioni 3D, usare [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
