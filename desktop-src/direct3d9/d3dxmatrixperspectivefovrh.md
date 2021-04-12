---
description: Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: Funzione D3DXMatrixPerspectiveFovRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da478a027db8c366a2cfec827075d3d4b73ae014
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355414"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a>Funzione D3DXMatrixPerspectiveFovRH (D3dx9math. h)

Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.

## <a name="syntax"></a>Sintassi


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
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

*fovy* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Campo di visualizzazione nella direzione y, in radianti.

</dd> <dt>

*Aspetto* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Proporzioni, definite come larghezza dello spazio di visualizzazione divisa per l'altezza.

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

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXMatrixPerspectiveFovRH** può essere utilizzata come parametro per un'altra funzione.

Per modificare l'asse delle proporzioni, usare la formula di calcolo: fovy = 2 * Math. Atan (Math. Tan (fovy * 0,5)/aspect). In alternativa, aggiungere variabili di proporzioni X e Y nella struttura per ridimensionare lo spazio di visualizzazione verticale: fovy = 2 * Math. Atan (Math. Tan (fovy * 0,5)/aspecty), aspect = aspectX * aspect Y.

Questa funzione calcola la matrice restituita come illustrato.


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
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

[**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
