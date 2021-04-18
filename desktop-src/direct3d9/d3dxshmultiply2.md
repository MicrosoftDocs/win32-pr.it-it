---
description: Calcola il prodotto di due funzioni rappresentate mediante SH (f e g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Funzione D3DXSHMultiply2 (D3dx9math. h)
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
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322474"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a>Funzione D3DXSHMultiply2 (D3dx9math. h)

Calcola il prodotto di due funzioni rappresentate mediante SH (f e g).

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

*broncio* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti SH di output. la funzione di base YLM è archiviata a l \* l + m + l.

</dd> <dt>

*PF* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Input SH coeffs per la prima funzione.

</dd> <dt>

*PG* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Secondo set di input SH coeffs.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH.

## <a name="remarks"></a>Commenti

L'ordine è un numero compreso tra 2 e 6 inclusi. Quindi, in questa pagina vengono effettivamente documentate diverse funzioni: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.

Calcola il prodotto di due funzioni rappresentate usando SH (f e g), dove *broncio* \[ i \] = int (y \_ i (s) f/s) \* \* , dove y \_ i/o è la funzione di base SH, f (s) e g/s sono funzioni SH (Sum \_ i (y i \_ \* \_ /sec)). L'ordine O determina le lunghezze delle matrici, in cui devono essere sempre presenti coefficienti O ^ 2. In generale, il prodotto di due funzioni SH dell'ordine O genera una funzione SH dell'ordine 2 \* O-1, ma i risultati vengono troncati. Ciò significa che il prodotto si sposta (f \* g = = g \* f) ma non associa (f \* (g \* h)! = (f \* g) \* h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
