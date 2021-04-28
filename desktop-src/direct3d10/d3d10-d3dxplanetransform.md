---
description: 'Funzione D3DXPlaneTransform (D3DX10Math.h): trasforma un piano in base a una matrice. La matrice di input è il trasposto inverso della trasformazione effettiva.'
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Funzione D3DXPlaneTransform (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b1d16ba2a29d42614c388a6207503ad32dd5e0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108789"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a>Funzione D3DXPlaneTransform (D3DX10Math.h)

Trasforma un piano in base a una matrice. La matrice di input è il trasposto inverso della trasformazione effettiva.

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

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntatore [**all'oggetto D3DXPLANE**](d3d10-d3dxplane.md) che contiene il piano trasformato risultante. Vedere l'esempio.

</dd> <dt>

*pP* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntatore alla struttura D3DXPLANE di input che contiene il piano che verrà trasformato. Il vettore (a,b,c) che descrive il piano deve essere normalizzato prima che venga chiamata questa funzione. Vedere l'esempio.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine, che contiene i valori di trasformazione. Questa matrice deve contenere il traspose inverso dei valori di trasformazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntatore a una struttura D3DXPLANE che rappresenta il piano trasformato. Si tratta dello stesso valore restituito nel parametro pOut in modo che questa funzione possa essere usata come parametro per un'altra funzione.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
