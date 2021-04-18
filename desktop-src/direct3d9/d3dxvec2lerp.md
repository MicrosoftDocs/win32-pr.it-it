---
description: Esegue un'interpolazione lineare tra due vettori 2D.
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: Funzione D3DXVec2Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08b767993143db3057985140b97854b9203d2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322459"
---
# <a name="d3dxvec2lerp-function"></a>D3DXVec2Lerp (funzione)

Esegue un'interpolazione lineare tra due vettori 2D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Parametro che esegue l'interpolazione lineare tra i vettori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che è il risultato dell'interpolazione lineare.

## <a name="remarks"></a>Commenti

Questa funzione esegue l'interpolazione lineare in base alla formula seguente: V1 + s (v2-v1).

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXVec2Lerp** può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
