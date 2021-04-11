---
description: Calcola il prodotto di due funzioni di armonica sferica (f e g). Entrambe le funzioni sono di ordine N = 4.
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: Funzione D3DXSHMultiply4 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13e8b62674ccbabbb03259f06b79f330424ddf84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235125"
---
# <a name="d3dxshmultiply4-function"></a>D3DXSHMultiply4 (funzione)

Calcola il prodotto di due funzioni di armonica sferica (*f* e *g*). Entrambe le funzioni sono di ordine N = 4.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHMultiply4(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti SH di output: la funzione di base *Y* LM è archiviata in l ² + *m* + l. L'ordine *N* determina la lunghezza della matrice, in cui devono essere sempre presenti coefficienti *n*².

</dd> <dt>

*PF* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Coefficienti SH di input per la prima funzione.

</dd> <dt>

*PG* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Secondo set di coefficienti SH di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH.

## <a name="remarks"></a>Commenti

Il prodotto di due funzioni SH dell'ordine N = 4 genera una funzione SH dell'ordine 2 × *N* -1 = 7, ma i risultati vengono troncati. Ciò significa che il prodotto si sposta ( *f* × *g*  =  *g* × *f* ) ma non associa ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).

Questa funzione usa l'equazione seguente:


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



dove y i \_ (s) è la funzione di base per i/o e dove f (s) e g (s) usano la funzione SH seguente:


```
sum_i(y_i(s)*c_i)
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

 

 
