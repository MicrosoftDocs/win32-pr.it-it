---
description: Calcola il prodotto scalare di due vettori a sferica armonica (SH).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Funzione D3DXSHDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a69ee929c889232cb29ff1b556dd08ab65a0d6d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401958"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a>Funzione D3DXSHDot (D3dx9math. h)

Calcola il prodotto scalare di due vettori a sferica armonica (SH).

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione dell'armonica sferica (SH). Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Coefficienti di output SH.

## <a name="remarks"></a>Commenti

Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:

-   l è il grado della funzione di base.
-   m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Trasferimento Radiance pre-calcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
