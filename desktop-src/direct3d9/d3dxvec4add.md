---
description: Aggiunge due vettori 4D.
ms.assetid: da807dc0-6a31-4315-a32d-a42062c22199
title: Funzione D3DXVec4Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62747cec15c4a9916dfb42572006cbb9fc908b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323373"
---
# <a name="d3dxvec4add-function"></a>D3DXVec4Add (funzione)

Aggiunge due vettori 4D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR4* D3DXVec4Add(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta la somma dei due vettori.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXVec4Add** può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Subtract**](d3dxvec4subtract.md)
</dt> <dt>

[**D3DXVec4Scale**](d3dxvec4scale.md)
</dt> </dl>

 

 




