---
description: 'Funzione D3DXSHAdd (D3dx9math.h): aggiunge due vettori sferici aricali (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Funzione D3DXSHAdd (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117959"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a>Funzione D3DXSHAdd (D3dx9math.h)

Aggiunge due vettori sferici aricali (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH. La valutazione genera coefficienti Di ordine. Vedere la sezione Osservazioni.

</dd> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

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
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Trasferimento di radiance pre-ricalcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
