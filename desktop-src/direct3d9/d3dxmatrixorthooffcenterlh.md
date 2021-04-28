---
description: 'Funzione D3DXMatrixOrthoOffCenterLH (D3dx9math.h): compila una matrice di proiezione ortografica personalizzata e mancino.'
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: Funzione D3DXMatrixOrthoOffCenterLH (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 704bdab1d486399b28117cd078f556beb1347f7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107489"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a>Funzione D3DXMatrixOrthoOffCenterLH (D3dx9math.h)

Compila una matrice di proiezione ortografica personalizzata mancino.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
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

*l* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore x minimo del volume di visualizzazione.

</dd> <dt>

*r* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore x massimo del volume di visualizzazione.

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore y minimo del volume della vista.

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore y massimo del volume della vista.

</dd> <dt>

*zn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z minimo del volume di visualizzazione.

</dd> <dt>

*zf* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore z massimo del volume di visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore all'oggetto [**D3DXMATRIX risultante.**](../direct3d10/d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Commenti

La [**funzione D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) è un caso speciale della **funzione D3DXMatrixOrthoOffCenterLH.** Per creare la stessa proiezione **usando D3DXMatrixOrthoOffCenterLH,** usare i valori seguenti: l = -w/2, r = w/2, b = -h/2 e t = h/2.

Tutti i parametri della **funzione D3DXMatrixOrthoOffCenterLH** sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume di visualizzazione.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixOrthoOffCenterLH** può essere usata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
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

[**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterRH**](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
