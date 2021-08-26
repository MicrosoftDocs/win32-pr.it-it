---
description: Calcola il prodotto di due funzioni aricali sferiche (f e g). Entrambe le funzioni sono di ordine N = 2.
ms.assetid: 9e0942ce-e39d-4147-9472-cda8a97fd390
title: Funzione D3DXSHMultiply2 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6fba685a763a00e529e70b7c0f08a97706f3c5f2be4dba7c923ed5b4b102742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070001"
---
# <a name="d3dxshmultiply2-function-d3dx10mathh"></a>Funzione D3DXSHMultiply2 (D3DX10Math.h)

Calcola il prodotto di due funzioni aricali sferiche (*f* e *g*). Entrambe le funzioni sono di ordine N = 2.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti SH di output: la funzione di base *Y* lm viene archiviata in l PIÙ + *m* + l. *L'ordine N* determina la lunghezza della matrice, in cui devono essere sempre presenti *coefficienti N* PIÙ.

</dd> <dt>

*pF* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Coefficienti SH di input per la prima funzione.

</dd> <dt>

*pG* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Secondo set di coefficienti SH di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH.

## <a name="remarks"></a>Commenti

Il prodotto di due funzioni SH dell'ordine N = 2 genera una funzione SH dell'ordine 2 × *N* - 1 = 3, ma i risultati vengono troncati. Ciò significa che il prodotto viene commutato ( *f* × *g* g × f ) ma non associa  =   ( *f* × (*g* × *h*) ≠ ( *f* × *g*) × *h* ). 

Questa funzione usa l'equazione seguente:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



dove y \_ i(s) è la funzione di base sh e dove f(s) e g(s) usano la funzione SH seguente:


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
