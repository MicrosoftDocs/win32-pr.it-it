---
description: "Funzione D3DXVec3Hermite (D3DX10Math.h): esegue un'interpolazione spline hermite usando i vettori 3D specificati."
ms.assetid: d2212299-0478-48a6-b303-60c212528058
title: Funzione D3DXVec3Hermite (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: cbed5ceaca1e4e404c47766fa41b8b095216b277
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108189"
---
# <a name="d3dxvec3hermite-function-d3dx10mathh"></a>Funzione D3DXVec3Hermite (D3DX10Math.h)

Esegue un'interpolazione spline hermite usando i vettori 3D specificati.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 di origine, un vettore di posizione.

</dd> <dt>

*pT1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 di origine, un vettore tangente.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 di origine, un vettore di posizione.

</dd> <dt>

*pT2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3 di origine, un vettore tangente.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a una struttura D3DXVECTOR3 che rappresenta il risultato dell'interpolazione spline hermite.

## <a name="remarks"></a>Commenti

La **funzione D3DXVec3Hermite** interpola da (positionA, tangentA) a (positionB, tangentB) usando l'interpolazione spline hermite.

L'interpolazione spline è una generalizzazione della spline semplice e semplice. La rampa è una funzione di Q(s) con le proprietà seguenti.

Q(s) = As i + Bs più Cs + D (e pertanto Q'(s) = 3As PIÙ + 2Bs + C)

a) Q(0) = v1, quindi Q'(0) = t1

b) Q(1) = v2, quindi Q'(1) = t2

v1 è il contenuto di pV1, v2 nel contenuto di pV2, t1 è il contenuto di pT1 e t2 è il contenuto di pT2.

Queste proprietà vengono usate per risolvere A, B, C, D.


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



Collegare le soluzioni per A, B, C e D per generare domande e risposte.


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



Il risultato è il seguente:

Q(s) = (2v1 - 2v2 + t2 + t1)s ° + (3v2 - 3v1 - 2t1 - t2)s più + t1s + v1

Che può essere ridisposto come:

Q(s) = (2s i - 3s più 1)v1 + (-2s più 3s 2)v2 + (sZIONI - 2s più s)t1 + (s ° - s più)t2

Le spline ermite sono utili per controllare l'animazione perché la curva attraversa tutti i punti di controllo. Inoltre, poiché la posizione e la tangente vengono specificate in modo esplicito alle estremità di ogni segmento, è facile creare una curva continua C2, purché la posizione iniziale e la tangente corrispondano ai valori finali dell'ultimo segmento.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXVec3Hermite** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
