---
description: 'Funzione D3DXMatrixOrthoOffCenterRH (D3DX10Math.h): crea una matrice di proiezione ortografica personalizzata con la mano destra.'
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: Funzione D3DXMatrixOrthoOffCenterRH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 79594b606124f6b3634e7b379bda0cb664cbec31b417112641d06f335a16ce04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541242"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a>Funzione D3DXMatrixOrthoOffCenterRH (D3DX10Math.h)

Compila una matrice di proiezione ortogonale personalizzata con la mano destra.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore all'oggetto [**D3DXMATRIX risultante.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Commenti

La [**funzione D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) è un caso speciale della funzione D3DXMatrixOrthoOffCenterRH. Per creare la stessa proiezione usando D3DXMatrixOrthoOffCenterRH, usare i valori seguenti:

l = -w/2,

r = w/2,

b = -h/2 e

t = h/2.

Tutti i parametri della funzione D3DXMatrixOrthoOffCenterRH sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume della vista.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXMatrixOrthoOffCenterRH può essere usata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
