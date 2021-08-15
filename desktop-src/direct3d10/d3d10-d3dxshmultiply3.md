---
description: Calcola il prodotto di due funzioni aricali sferiche (f e g). Entrambe le funzioni sono di ordine N = 3.
ms.assetid: 2845f90f-c8a0-4ca9-b2f6-7491a2b4763b
title: Funzione D3DXSHMultiply3 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply3
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a04e4979d412a4533b74c7d7610933527c2bdaacb9733b9eb08c6e0ad56e4e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990811"
---
# <a name="d3dxshmultiply3-function"></a>Funzione D3DXSHMultiply3

Calcola il prodotto di due funzioni aricali sferiche (*f* e *g*). Entrambe le funzioni sono di ordine N = 3.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHMultiply3(
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

Il prodotto di due funzioni SH dell'ordine N = 3 genera una funzione SH di ordine 2 × *N* - 1 = 5, ma i risultati vengono troncati. Ciò significa che il prodotto viene commutato ( *f* × *g* g × f ) ma non associa  =   ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ). 

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

 

 
