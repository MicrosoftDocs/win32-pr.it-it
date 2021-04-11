---
description: Crea una matrice di proiezione prospettica destrorsa.
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: Funzione D3DXMatrixPerspectiveRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcec04202ecb2de15c479ac4ce84d4ee86c99a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234945"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a>Funzione D3DXMatrixPerspectiveRH (D3dx9math. h)

Crea una matrice di proiezione prospettica destrorsa.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
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

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Larghezza del volume di visualizzazione nel piano di visualizzazione vicino.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Altezza del volume di visualizzazione nel piano di visualizzazione vicino.

</dd> <dt>

*Zn* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore Z del piano di visualizzazione vicino.

</dd> <dt>

*ZF* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore Z del piano di visualizzazione lontano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica a destra.

## <a name="remarks"></a>Commenti

Tutti i parametri della funzione **D3DXMatrixPerspectiveRH** sono distanze nello spazio della fotocamera. I parametri descrivono le dimensioni del volume di visualizzazione.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXMatrixPerspectiveRH** può essere utilizzata come parametro per un'altra funzione.

Questa funzione usa la formula seguente per calcolare la matrice restituita.


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
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

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
