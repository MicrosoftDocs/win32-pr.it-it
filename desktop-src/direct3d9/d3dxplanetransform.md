---
description: Trasforma un piano in base a una matrice. La matrice di input è la trasposta inversa della trasformazione effettiva.
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: Funzione D3DXPlaneTransform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd82478d9fb1f08bb0320a8c84357efcdf20be26
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322096"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a>Funzione D3DXPlaneTransform (D3dx9math. h)

Trasforma un piano in base a una matrice. La matrice di input è la trasposta inversa della trasformazione effettiva.

## <a name="syntax"></a>Sintassi


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che contiene il piano trasformato risultante. Vedere l'esempio.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore alla struttura di input [**D3DXPLANE**](d3dxplane.md) , che contiene il piano che verrà trasformato. Il vettore (a, b, c) che descrive il piano deve essere normalizzato prima che questa funzione venga chiamata. Vedere l'esempio.

</dd> <dt>

*PM* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine, che contiene i valori della trasformazione. Questa matrice deve contenere la trasposta inversa dei valori della trasformazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il piano trasformato. Si tratta dello stesso valore restituito nel parametro broncio, in modo che questa funzione possa essere utilizzata come parametro per un'altra funzione.

## <a name="remarks"></a>Commenti

### <a name="examples"></a>Esempi

Questo esempio trasforma un piano applicando una scala non uniforme.


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



Un piano è descritto da AX + + + CZ + DW = 0. Il primo piano viene creato con (a, b, c, d) = (0, 1, 1, 0), che è un piano descritto da y + z = 0. Dopo la scalabilità, il nuovo piano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f,0), che mostra il nuovo piano da descrivere con 0.353 y + 0.235 z = 0.

Il parametro pM contiene la trasposta inversa della matrice di trasformazione. La trasposta inversa è richiesta da questo metodo, in modo che sia possibile trasformare correttamente anche il vettore normale del piano trasformato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneNormalize**](d3dxplanenormalize.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> <dt>

[**D3DXMatrixInverse**](d3dxmatrixinverse.md)
</dt> <dt>

[**D3DXMatrixTranspose**](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




