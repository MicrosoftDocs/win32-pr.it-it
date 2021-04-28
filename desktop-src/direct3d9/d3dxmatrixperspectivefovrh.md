---
description: 'Funzione D3DXMatrixPerspectiveFovRH (D3dx9math.h): crea una matrice di proiezione prospettica con mano destra basata su un campo di visualizzazione.'
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: Funzione D3DXMatrixPerspectiveFovRH (D3dx9math.h)
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
ms.openlocfilehash: e8860a5d9fed13e8acdedfe67ed94a97911a6de0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118329"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a>Funzione D3DXMatrixPerspectiveFovRH (D3dx9math.h)

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*fovy* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Campo di visualizzazione nella direzione y, espresso in radianti.

</dd> <dt>

*Aspetto* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Proporzioni, definite come larghezza dello spazio di visualizzazione divisa per altezza.

</dd> <dt>

*zn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore Z del piano di visualizzazione vicino.

</dd> <dt>

*zf* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore Z del piano di visualizzazione lontano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica con la mano destra.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXMatrixPerspectiveFovRH** può essere usata come parametro per un'altra funzione.

Per modificare l'asse delle proporzioni, usare la formula di calcolo: fovy = 2 * math.atan(math.tan(fovy * 0,5) /aspect). In alternativa, aggiungere le variabili delle proporzioni X e Y nella struttura per ridimensionare lo spazio di visualizzazione verticale: fovy = 2 * math.atan(math.tan(fovy * 0.5) /aspectY), aspect = aspectX * aspect Y.

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
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



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

 

 
