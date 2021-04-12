---
description: Compila una matrice di proiezione prospettica personalizzata e a destra.
ms.assetid: e6826e46-fc80-41fa-b0d8-45b6797df76f
title: Funzione D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c4f211c6f57f60f8399fb5639edd07c3fc02377
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235138"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx9mathh"></a>Funzione D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h)

Compila una matrice di proiezione prospettica personalizzata e a destra.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
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

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*l* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore x minimo del volume di visualizzazione.

</dd> <dt>

*r* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore x massimo del volume di visualizzazione.

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore y minimo del volume di visualizzazione.

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore y massimo del volume di visualizzazione.

</dd> <dt>

*Zn* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore z minimo del volume di visualizzazione.

</dd> <dt>

*ZF* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore z massimo del volume di visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che è una matrice di proiezione prospettica personalizzata e a destra.

## <a name="remarks"></a>Commenti

Tutti i parametri della funzione **D3DXMatrixPerspectiveOffCenterRH** sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume di visualizzazione.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXMatrixPerspectiveOffCenterRH** può essere utilizzata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
