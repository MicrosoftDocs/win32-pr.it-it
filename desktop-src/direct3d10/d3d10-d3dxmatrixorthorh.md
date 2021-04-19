---
description: Compila una matrice di proiezione ortogonale a destra.
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: Funzione D3DXMatrixOrthoRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a8883f2690fa5a5f0bfa1bb1570163b714974b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323212"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a>Funzione D3DXMatrixOrthoRH (D3DX10Math. h)

Compila una matrice di proiezione ortogonale a destra.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)risultante.

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Larghezza del volume di visualizzazione.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Altezza del volume di visualizzazione.

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

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore al [**D3DXMATRIX**](d3d10-d3dxmatrix.md)risultante.

## <a name="remarks"></a>Commenti

Tutti i parametri della funzione D3DXMatrixOrthoRH sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume di visualizzazione.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione D3DXMatrixOrthoRH può essere utilizzata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
