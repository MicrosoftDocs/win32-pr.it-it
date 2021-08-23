---
description: Funzione D3DXSHAdd (D3DX10.h) - Aggiunge due vettori armonici sferici (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Funzione D3DXSHAdd (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f59d0d83424039af6d2ca5d4ea6ca25702d6fc50039502fb0af0eae3ab782ec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990931"
---
# <a name="d3dxshadd-function-d3dx10h"></a>Funzione D3DXSHAdd (D3DX10.h)

Aggiunge due vettori armoniosi sferici (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH. La valutazione genera coefficienti Order². Vedere la sezione Osservazioni.

</dd> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo tra D3DXSH \_ MINORDER e D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Order². Il grado di valutazione è Order - 1.

</dd> <dt>

*pA* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntatore al primo vettore SH.

</dd> <dt>

*pB* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntatore al secondo vettore SH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH.

## <a name="remarks"></a>Commenti

Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l² + m + l, dove:

-   l è il grado della funzione di base.
-   m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
