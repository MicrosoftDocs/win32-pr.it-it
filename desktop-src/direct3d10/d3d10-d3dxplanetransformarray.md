---
description: Trasforma una matrice di piani in base a una matrice. È necessario normalizzare i vettori che descrivono ogni piano.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Funzione D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058646"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>Funzione D3DXPlaneTransformArray (D3DX10Math. h)

Trasforma una matrice di piani in base a una matrice. È necessario normalizzare i vettori che descrivono ogni piano.

## <a name="syntax"></a>Sintassi


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntatore alla struttura [**D3DXPLANE**](d3d10-d3dxplane.md) che contiene il piano trasformato risultante. Vedere l'esempio.

</dd> <dt>

*Outstride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride di ogni piano trasformato.

</dd> <dt>

*PP* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Puntatore alla struttura di input D3DXPLANE, che contiene la matrice di piani da trasformare. Il vettore (a, b, c) che descrive il piano deve essere normalizzato prima che questa funzione venga chiamata. Vedere l'esempio.

</dd> <dt>

*PStride* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride di ogni piano non trasformato.

</dd> <dt>

*PM* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine, che contiene la trasposta inversa dei valori della trasformazione.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di piani da trasformare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Puntatore a una struttura D3DXPLANE che rappresenta il piano trasformato. Si tratta dello stesso valore restituito nel parametro broncio, in modo che questa funzione possa essere utilizzata come parametro per un'altra funzione.

## <a name="remarks"></a>Commenti

Questo esempio trasforma un piano applicando una scala non uniforme.


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



Un piano è descritto da AX + + + CZ + DW = 0. Il primo piano viene creato con (a, b, c, d) = (0, 1, 1, 0), che è un piano descritto da y + z = 0. Dopo la scalabilità, il nuovo piano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f,0), che mostra il nuovo piano da descrivere con 0.353 y + 0.235 z = 0.

Il parametro pM contiene la trasformazione inversa della matrice di trasformazione. La trasposta inversa è richiesta da questo metodo, in modo che sia possibile trasformare correttamente anche il vettore normale del piano trasformato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
