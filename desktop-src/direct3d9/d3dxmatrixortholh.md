---
description: 'Funzione D3DXMatrixOrthoLH (D3dx9math.h): crea una matrice di proiezione ortografica mancino.'
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: Funzione D3DXMatrixOrthoLH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5492a6caba87025d83562c0327ac0e1f5a76f269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107499"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a>Funzione D3DXMatrixOrthoLH (D3dx9math.h)

Compila una matrice di proiezione ortografica mancino.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Larghezza del volume di visualizzazione.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Altezza del volume di visualizzazione.

</dd> <dt>

*zn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z minimo del volume di visualizzazione, definito z-near.

</dd> <dt>

*zf* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z massimo del volume di visualizzazione, definito z-far.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Commenti

Tutti i parametri della **funzione D3DXMatrixOrthoLH** sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume della vista.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixOrthoLH** può essere usata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterRH**](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterLH**](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
