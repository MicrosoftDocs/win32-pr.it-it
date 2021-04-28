---
description: 'Funzione D3DXMatrixTransformation2D (D3dx9math.h): compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano xy. Gli argomenti NULL vengono trattati come trasformazioni di identità.'
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Funzione D3DXMatrixTransformation2D (D3dx9math.h)
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
ms.openlocfilehash: b92a5489569765ef059af9b1023b40fc681b5d0c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098119"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>Funzione D3DXMatrixTransformation2D (D3dx9math.h)

Compila una matrice di trasformazione 2D che rappresenta le trasformazioni nel piano xy. **Gli** argomenti NULL vengono trattati come trasformazioni di identità.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore [**alla struttura D3DXMATRIX**](d3dxmatrix.md) che contiene il risultato delle trasformazioni.

</dd> <dt>

*pScalingCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una [**struttura D3DXVECTOR2,**](d3dxvector2.md) un punto che identifica il centro di ridimensionamento. Se questo argomento è **NULL,** viene applicata un'identità M <sub>sc</sub> matrix alla formula in Osservazioni.

</dd> <dt>

*pScalingRotation* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di rotazione di ridimensionamento.

</dd> <dt>

*pScaling* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a [**una struttura D3DXVECTOR2,**](d3dxvector2.md) un punto che identifica la scala. Se questo argomento è **NULL,** una matrice Identity Ms viene applicata alla formula in Osservazioni.

</dd> <dt>

*pRotationCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a [**una struttura D3DXVECTOR2,**](d3dxvector2.md) un punto che identifica il centro di rotazione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice identity M <sub>rc.</sub>

</dd> <dt>

*Rotazione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Angolo di rotazione in radianti.

</dd> <dt>

*pTranslation* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a [**una struttura D3DXVECTOR2,**](d3dxvector2.md) che identifica la conversione. Se questo argomento è **NULL,** alla formula in Osservazioni viene applicata una matrice Identity Mt.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che contiene la matrice di trasformazione.

## <a name="remarks"></a>Commenti

Questa funzione calcola la matrice di trasformazione con la formula seguente, con la concatenazione di matrici valutata in ordine da sinistra a destra:

M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹ \* Ms \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mt

dove:

M <sub>out</sub> = matrice di output (*pOut*)

M <sub>sc</sub> = scalabilità della matrice centrale (*pScalingCenter*)

M <sub>sr</sub> = scalare la matrice di rotazione (*pScalingRotation*)

Ms = matrice di ridimensionamento (*pScaling*)

M <sub>rc</sub> = centro della matrice di rotazione (*pRotationCenter*)

M <sub>r</sub> = matrice di rotazione (*rotazione*)

Mt = matrice di traslazione (*pTranslation*)

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXMatrixTransformation2D** può essere usata come parametro per un'altra funzione.

Per le trasformazioni 3D, usare [**D3DXMatrixTransformation.**](d3dxmatrixtransformation.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
