---
description: Esegue un'interpolazione di Catmull-Rom, usando i vettori 2D specificati.
ms.assetid: 8ec1abfa-0fa9-486a-b86d-bbb8f1d63849
title: Funzione D3DXVec2CatmullRom (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CatmullRom
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 71f499313a31c200b5cc657664b10b43dde47ba6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323192"
---
# <a name="d3dxvec2catmullrom-function-d3dx10mathh"></a>Funzione D3DXVec2CatmullRom (D3DX10Math. h)

Esegue un'interpolazione di Catmull-Rom, usando i vettori 2D specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR2* D3DXVec2CatmullRom(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV0,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV0* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.

</dd> <dt>

*pV3* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore a una struttura D3DXVECTOR2 che è il risultato dell'interpolazione del Catmull-Rom.

## <a name="remarks"></a>Commenti

Dato quattro punti (P1, P2, P3, P4), trovare una funzione Q (s) in modo che:


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



È possibile derivare la spline Catmull-Rom dalla spline eremita impostando:


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



dove:

V1 è il contenuto di pV0.

V2 è il contenuto di pV1.

P3 è il contenuto di pV2.

P4 è il contenuto di pV3.

Uso dell'equazione spline eremita:


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



e sostituendo V1, V2, T1, T2 restituisce:


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



Questo può essere ridisposto come segue:


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
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

 

 
