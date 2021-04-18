---
description: Aggiunge due valori di colore per creare un nuovo valore di colore.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Funzione D3DXColorAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323015"
---
# <a name="d3dxcoloradd-function"></a>D3DXColorAdd (funzione)

Aggiunge due valori di colore per creare un nuovo valore di colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.

</dd> <dt>

*pC1* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.

</dd> <dt>

*pC2* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è la somma di due valori di colore.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito in broncio. In questo modo, la funzione **D3DXColorAdd** può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorSubtract**](d3dxcolorsubtract.md)
</dt> </dl>

 

 




