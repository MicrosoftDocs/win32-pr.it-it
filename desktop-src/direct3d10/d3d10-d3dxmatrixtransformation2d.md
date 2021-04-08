---
description: Compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano XY. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Funzione D3DXMatrixTransformation2D (D3DX10Math. h)
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
ms.openlocfilehash: b41d8234dcd9dda1b3735c83460a20c7109e63d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762274"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>Funzione D3DXMatrixTransformation2D (D3DX10Math. h)

Compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano XY. Gli argomenti **null** vengono considerati come trasformazioni di identità.

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

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che contiene il risultato delle trasformazioni.

</dd> <dt>

*pScalingCenter* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a un [**D3DXVECTOR2**](d3d10-d3dxvector2.md), un punto che identifica il centro di ridimensionamento. Se questo argomento è **null**, una matrice Identity M <sub>SC</sub> viene applicata alla formula nei commenti.

</dd> <dt>

*ScalingRotation* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Puntatore al fattore di rotazione di ridimensionamento.

</dd> <dt>

*pScaling* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2, un punto che identifica la scala. Se questo argomento è **null**, una matrice di identità MS viene applicata alla formula nei commenti.

</dd> <dt>

*pRotationCenter* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2, un punto che identifica il centro della rotazione. Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*Rotazione* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Angolo di rotazione in radianti.

</dd> <dt>

*pTranslation* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2, che identifica la traduzione. Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX che contiene la matrice di trasformazione.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* M<sub>r</sub> \* m<sub>RC</sub> \* mt

dove:

M<sub>out</sub> = matrice di output (broncio)

M<sub>SC</sub> = scala Center Matrix (pScalingCenter)

M<sub>Sr</sub> = scala della matrice di rotazione (pScalingRotation)

MS = scala Matrix (pScaling)

M<sub>RC</sub> = matrice Center of rotation (pRotationCenter)

M<sub>r</sub> = matrice di rotazione (rotazione)

Mt = matrice di traslazione (pTranslation)

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione D3DXMatrixTransformation2D può essere utilizzata come parametro per un'altra funzione.

Per le trasformazioni 3D, usare [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
