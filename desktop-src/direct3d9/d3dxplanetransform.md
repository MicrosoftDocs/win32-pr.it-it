---
description: 'Funzione D3DXPlaneTransform (D3dx9math.h): trasforma un piano in base a una matrice. La matrice di input è la trasposizione inversa della trasformazione effettiva.'
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: Funzione D3DXPlaneTransform (D3dx9math.h)
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
ms.openlocfilehash: c4376319d8ac2d49c480110d5119af5a3cefc9fe491f4997efdc15e30bf50db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986461"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a>Funzione D3DXPlaneTransform (D3dx9math.h)

Trasforma un piano in base a una matrice. La matrice di input è la trasposizione inversa della trasformazione effettiva.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore alla [**struttura D3DXPLANE**](d3dxplane.md) che contiene il piano trasformato risultante. Vedere l'esempio.

</dd> <dt>

*pP* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) di input, che contiene il piano che verrà trasformato. Il vettore (a,b,c) che descrive il piano deve essere normalizzato prima che venga chiamata questa funzione. Vedere l'esempio.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine, che contiene i valori della trasformazione. Questa matrice deve contenere la trasposizione inversa dei valori di trasformazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Puntatore a [**una struttura D3DXPLANE,**](d3dxplane.md) che rappresenta il piano trasformato. Si tratta dello stesso valore restituito nel parametro pOut in modo che questa funzione possa essere usata come parametro per un'altra funzione.

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



Un piano è descritto da ax + by + cz + dw = 0. Il primo piano viene creato con (a,b,c,d) = (0,1,1,0), ovvero un piano descritto da y + z = 0. Dopo il ridimensionamento, il nuovo piano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), che mostra il nuovo piano descritto da 0,353y + 0,235z = 0.

Il parametro pM contiene la trasposizione inversa della matrice di trasformazione. La trasposizione inversa è richiesta da questo metodo in modo che anche il vettore normale del piano trasformato possa essere trasformato correttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



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

 

 




