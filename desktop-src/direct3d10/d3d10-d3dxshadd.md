---
description: Aggiunge due vettori ad armonica sferica (SH); in altre parole, broncio \[ i \] = PA i \[ \] + PB \[ i \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Funzione D3DXSHAdd (D3DX10. h)
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
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235155"
---
# <a name="d3dxshadd-function-d3dx10h"></a>Funzione D3DXSHAdd (D3DX10. h)

Aggiunge due vettori ad armonica sferica (SH); in altre parole, broncio \[ i \] = PA i \[ \] + PB \[ i \] .

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

*broncio* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH. La valutazione genera coefficienti Order ². Vedere la sezione Osservazioni.

</dd> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*PA* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntatore al primo vettore SH.

</dd> <dt>

*PB* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntatore al secondo vettore SH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH.

## <a name="remarks"></a>Commenti

Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:

-   l è il grado della funzione di base.
-   m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
