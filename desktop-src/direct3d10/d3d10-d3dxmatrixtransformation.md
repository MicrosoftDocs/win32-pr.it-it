---
description: 'Funzione D3DXMatrixTransformation (D3DX10Math.h): compila una matrice di trasformazione. Gli argomenti NULL vengono trattati come trasformazioni di identità.'
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: Funzione D3DXMatrixTransformation (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a9f9b6679093ef1defb98289bbc1c0f70410a7ab6b1f4c7a5107012e16976a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754311"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a>Funzione D3DXMatrixTransformation (D3DX10Math.h)

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pScalingCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a un [**oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md)che identifica il punto centrale di ridimensionamento. Se questo argomento è **NULL,** viene applicata alla formula un'identità M <sub>sc</sub> matrix nelle osservazioni.

</dd> <dt>

*pScalingRotation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore a [**un oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che specifica la rotazione di ridimensionamento. Se questo argomento è **NULL,** una matrice identity M <sub>sr</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*pScaling* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3, il vettore di ridimensionamento. Se questo argomento è **NULL,** una matrice Identity Ms viene applicata alla formula in Osservazioni.

</dd> <dt>

*pRotationCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3, un punto che identifica il centro di rotazione. Se questo argomento è **NULL,** una matrice identity M <sub>rc</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*pRotation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore a una struttura D3DXQUATERNION che specifica la rotazione. Se questo argomento è **NULL,** una matrice di identità M <sub>r</sub> viene applicata alla formula nelle osservazioni.

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 che rappresenta la traslazione. Se questo argomento è **NULL,** viene applicata una matrice Identity Mt alla formula in Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a una struttura D3DXMATRIX che rappresenta la matrice di trasformazione.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione con la formula seguente, con la concatenazione di matrici valutata nell'ordine da sinistra a destra:

M<sub>out</sub> = (M<sub>sc</sub>)⁻ più \* (M<sub>sr</sub>)⁻ ms \* M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻⁻ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

dove:

M<sub>out</sub> = matrice di output (pOut)

M<sub>sc</sub> = matrice del centro di ridimensionamento (pScalingCenter)

M<sub>sr</sub> = matrice di rotazione di ridimensionamento (pScalingRotation)

Ms = matrice di ridimensionamento (pScaling)

M<sub>rc</sub> = centro della matrice di rotazione (pRotationCenter)

M<sub>r</sub> = matrice di rotazione (pRotation)

Mt = matrice di traslazione (pTranslation)

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixTransformation può essere usata come parametro per un'altra funzione.

Per le trasformazioni 2D, usare [**D3DXMatrixTransformation2D.**](d3d10-d3dxmatrixtransformation2d.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
