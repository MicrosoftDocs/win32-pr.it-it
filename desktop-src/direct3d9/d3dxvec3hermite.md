---
description: Esegue un'interpolazione spline eremita, usando i vettori 3D specificati.
ms.assetid: d45b1179-0e11-4f58-8d50-432236cb88ca
title: Funzione D3DXVec3Hermite (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b5609215d0ab56e9d91979d01f996981b2ffcbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323294"
---
# <a name="d3dxvec3hermite-function-d3dx9mathh"></a>Funzione D3DXVec3Hermite (D3dx9math. h)

Esegue un'interpolazione spline eremita, usando i vettori 3D specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine, un vettore di posizione.

</dd> <dt>

*pt1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine, un vettore tangente.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine, un vettore di posizione.

</dd> <dt>

*PT2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine, un vettore tangente.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che è il risultato dell'interpolazione della spline eremita.

## <a name="remarks"></a>Commenti

La funzione **D3DXVec3Hermite** esegue l'interpolazione da (PositionA, tangentea) a (PositionB, tangentB) usando l'interpolazione spline eremita.

L'interpolazione spline è una generalizzazione della spline di Ease-Out. La rampa è una funzione di Q (s) con le proprietà seguenti.

Q (s) = come ³ + BS ² + CS + D (e quindi Q '/s = 3As ² + 2B + C)

a) Q (0) = V1, quindi Q ' (0) = T1

b) Q (1) = V2, quindi Q ' (1) = T2

V1 è il contenuto di pV1, V2 nel contenuto di pV2, T1 è il contenuto di pT1 e T2 è il contenuto di pT2.

Queste proprietà vengono utilizzate per la risoluzione di un oggetto, B, C, D.

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

Collegare le soluzioni per a, B, C e D per generare Q (s).

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

Il risultato è il seguente:

Q (s) = (2V1-2v2 + T2 + T1) s ³ + (3V2-3V1-2T1-T2) s ² + T1s + V1

Che può essere ridisposto come segue:

Q (s) = (2S ³-3S ² + 1) V1 + (-2S ³ + 3S ²) V2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2

Le spline di eremita sono utili per controllare l'animazione perché la curva viene eseguita attraverso tutti i punti di controllo. Inoltre, poiché la posizione e la tangente vengono specificate in modo esplicito alle estremità di ogni segmento, è facile creare una curva C2 continua, purché si assicuri che la posizione iniziale e la tangente corrispondano ai valori finali dell'ultimo segmento.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXVec3Hermite** può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
