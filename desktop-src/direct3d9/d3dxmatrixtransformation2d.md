---
description: Compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano XY. Gli argomenti NULL vengono considerati come trasformazioni di identità.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Funzione D3DXMatrixTransformation2D (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322636"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>Funzione D3DXMatrixTransformation2D (D3dx9math. h)

Compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano XY. Gli argomenti **null** vengono considerati come trasformazioni di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
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

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che contiene il risultato delle trasformazioni.

</dd> <dt>

*pScalingCenter* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , un punto che identifica il centro di ridimensionamento. Se questo argomento è **null**, una matrice Identity M <sub>SC</sub> viene applicata alla formula nei commenti.

</dd> <dt>

*pScalingRotation* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di rotazione di ridimensionamento.

</dd> <dt>

*pScaling* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , un punto che identifica la scala. Se questo argomento è **null**, una matrice di identità MS viene applicata alla formula nei commenti.

</dd> <dt>

*pRotationCenter* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , un punto che identifica il centro della rotazione. Se questo argomento è **null**, una matrice Identity M <sub>RC</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*Rotazione* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Angolo di rotazione in radianti.

</dd> <dt>

*pTranslation* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) , che identifica la traduzione. Se questo argomento è **null**, viene applicata una matrice di valori Identity mt alla formula nei commenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che contiene la matrice di trasformazione.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione con la formula seguente, con concatenazione di matrici valutata in ordine da sinistra a destra:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* m<sub>SR</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* M<sub>r</sub> \* m<sub>RC</sub> \* mt

dove:

M <sub>out</sub> = matrice di output (*broncio*)

M <sub>SC</sub> = scala Center Matrix (*pScalingCenter*)

M <sub>Sr</sub> = scala della matrice di rotazione (*pScalingRotation*)

MS = scala Matrix (*pScaling*)

M <sub>RC</sub> = matrice Center of rotation (*pRotationCenter*)

M <sub>r</sub> = matrice di rotazione (*rotazione*)

Mt = matrice di traslazione (*pTranslation*)

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXMatrixTransformation2D** può essere utilizzata come parametro per un'altra funzione.

Per le trasformazioni 3D, usare [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
