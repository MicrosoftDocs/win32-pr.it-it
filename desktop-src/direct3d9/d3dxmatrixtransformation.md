---
description: 'Funzione D3DXMatrixTransformation (D3dx9math.h): compila una matrice di trasformazione. Gli argomenti NULL vengono trattati come trasformazioni di identità.'
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Funzione D3DXMatrixTransformation (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc3b6502a8015564207f208166cec15227d3b18a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098129"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a>Funzione D3DXMatrixTransformation (D3dx9math.h)

Compila una matrice di trasformazione. **Gli** argomenti NULL vengono trattati come trasformazioni di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
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

*pScalingCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) che identifica il punto centrale di ridimensionamento. Se questo argomento è **NULL,** viene applicata alla formula un'identità M <sub>sc</sub> matrix nelle osservazioni.

</dd> <dt>

*pScalingRotation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una [**struttura D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione di ridimensionamento. Se questo argomento è **NULL,** una matrice identity M <sub>sr</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*pScaling* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una [**struttura D3DXVECTOR3,**](d3dxvector3.md) il vettore di ridimensionamento. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Ms.

</dd> <dt>

*pRotationCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) un punto che identifica il centro di rotazione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>rc.</sub>

</dd> <dt>

*pRotation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che specifica la rotazione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>r.</sub>

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che rappresenta la traslazione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Mt.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di trasformazione.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione con la formula seguente, con la concatenazione di matrici valutata in ordine da sinistra a destra:

M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

dove:

M <sub>out</sub> = matrice di output (*pOut*)

M <sub>sc</sub> = scalabilità della matrice centrale (*pScalingCenter*)

M <sub>sr</sub> = scalare la matrice di rotazione (*pScalingRotation*)

Ms = matrice di ridimensionamento (*pScaling*)

M <sub>rc</sub> = centro della matrice di rotazione (*pRotationCenter*)

M <sub>r</sub> = matrice di rotazione (*pRotation*)

Mt = matrice di traslazione (*pTranslation*)

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixTransformation** può essere usata come parametro per un'altra funzione.

Per le trasformazioni 2D, usare [**D3DXMatrixTransformation2D.**](d3dxmatrixtransformation2d.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




