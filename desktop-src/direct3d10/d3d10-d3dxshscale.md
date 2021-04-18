---
description: Ridimensiona un vettore armonico sferico (SH); in altre parole, il broncio \[ i \] = PA \[ i \] \* scalare.
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: Funzione D3DXSHScale (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7aa7ee66b29c7d9816708a8625bb568426a62b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323329"
---
# <a name="d3dxshscale-function-d3dx10h"></a>Funzione D3DXSHScale (D3DX10. h)

Ridimensiona un vettore armonico sferico (SH); in altre parole, il broncio \[ i \] = PA \[ i \] \* scalare.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output armonici sferici (SH). La valutazione genera coefficienti Order ². Vedere la sezione Osservazioni.

</dd> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*Aggiungi* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntatore al vettore SH da scalare.

</dd> <dt>

*Ridimensiona* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md)**

Puntatore al valore della scala.

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

 

 
