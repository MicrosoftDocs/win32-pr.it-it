---
description: Crea il valore del colore negativo di un valore di colore.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Funzione D3DXColorNegative (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322881"
---
# <a name="d3dxcolornegative-function"></a>D3DXColorNegative (funzione)

Crea il valore del colore negativo di un valore di colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.

</dd> <dt>

*computer* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che corrisponde al valore di colore negativo del valore del colore.

## <a name="remarks"></a>Commenti

Il canale alfa di input viene copiato, non modificato, nel canale alfa di output.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXColorNegative** può essere utilizzata come parametro per un'altra funzione.

Questa funzione restituisce il valore di colore negativo sottraendo 1,0 dai componenti colore della struttura [**D3DXCOLOR**](d3dxcolor.md) , come illustrato nell'esempio seguente.


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




