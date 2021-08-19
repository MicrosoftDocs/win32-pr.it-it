---
description: Calcola il prodotto di due funzioni rappresentate usando SH (f e g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Funzione D3DXSHMultiply2 (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 00219ed1c38105562591b63e6bef64b949b2ab4443aed68e0e6b9d64cb156cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849691"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>Funzione D3DXSHMultiply2 (D3dx9math.h)

Calcola il prodotto di due funzioni rappresentate usando SH (f e g).

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

Puntatore ai coefficienti SH di output: la funzione base Ylm viene archiviata in \* l + m+l.

</dd> <dt>

*pF* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Input SH coeffs per la prima funzione.

</dd> <dt>

*pG* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Secondo set di coeff SH di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH.

## <a name="remarks"></a>Commenti

L'ordine è un numero compreso tra 2 e 6 inclusi. Questa pagina documenta in realtà diverse funzioni: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.

Calcola il prodotto di due funzioni rappresentate usando SH (f e g), dove *pOut* \[ i = \] int(y \_ \* i(s) f(s) \* f(s) g(s)), dove y \_ i(s) è l'ith SH basis function, f(s) e g(s) sono funzioni SH (sum \_ i(y \_ i(s) \* c \_ i)). L'ordine O determina le lunghezze delle matrici, in cui devono essere sempre presenti coefficienti O^2. In generale, il prodotto di due funzioni SH di ordine O genera una funzione SH di ordine 2 O - 1, ma i \* risultati vengono troncati. Ciò significa che il prodotto viene commutato (f g == g f) ma non associa \* \* (f \* (g \* h) != (f \* g) \* h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
