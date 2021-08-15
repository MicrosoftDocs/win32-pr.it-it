---
description: "Funzione D3DXVec2Hermite (D3DX10Math.h): esegue un'interpolazione spline hermite usando i vettori 2D specificati."
ms.assetid: 2d6ff836-a1a7-4cd0-aea3-4fe344f4e211
title: Funzione D3DXVec2Hermite (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 60e4aef5183e7c107b0853794b9e63c288916763daa4784e21241d55c1bfec89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990711"
---
# <a name="d3dxvec2hermite-function-d3dx10mathh"></a>Funzione D3DXVec2Hermite (D3DX10Math.h)

Esegue un'interpolazione spline hermite usando i vettori 2D specificati.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore [**all'oggetto D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.

</dd> <dt>

*pT1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore tangente.

</dd> <dt>

*pV2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.

</dd> <dt>

*pT2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Puntatore a una struttura D3DXVECTOR2 di origine, un vettore tangente.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di ponderazione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***

Puntatore a una struttura D3DXVECTOR2 che è il risultato dell'interpolazione spline hermite.

## <a name="remarks"></a>Commenti

La **funzione D3DXVec2Hermite** interpola da (positionA, tangentA) a (positionB, tangentB) usando l'interpolazione spline hermite.

L'interpolazione spline è una generalizzazione della spline ease-in e ease-out. La rampa è una funzione di Q(s) con le proprietà seguenti.

Q(s) = As² + Bs² + Cs + D (e pertanto, Q(s) = 3As² + 2Bs + C)

a) Q(0) = v1, quindi Q'(0) = t1

b) Q(1) = v2, quindi Q'(1) = t2

v1 è il contenuto di pV1, v2 nel contenuto di pV2, t1 è il contenuto di pT1 e t2 è il contenuto di pT2.

Queste proprietà vengono usate per risolvere A, B, C, D.


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
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

Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1

Che può essere ridisporto come:

Q(s) = (2s² - 3s² + 1)v1 + (-2s² + 3s²)v2 + (s³ - 2s² + s)t1 + (s² - s²)t2

Le spline ermeti sono utili per controllare l'animazione perché la curva attraversa tutti i punti di controllo. Inoltre, poiché la posizione e la tangente vengono specificate in modo esplicito alle estremità di ogni segmento, è facile creare una curva continua C2, purché la posizione iniziale e la tangente corrispondano ai valori finali dell'ultimo segmento.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXVec2Hermite** può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
