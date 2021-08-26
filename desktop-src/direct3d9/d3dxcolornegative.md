---
description: Crea il valore di colore negativo di un valore di colore.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Funzione D3DXColorNegative (D3dx9math.h)
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
ms.openlocfilehash: c046702b81ce60f2e50817cb98c04686d9a35e964a141d88fd70dd05654e3067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069331"
---
# <a name="d3dxcolornegative-function"></a>Funzione D3DXColorNegative

Crea il valore di colore negativo di un valore di colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pC* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntatore a una [**struttura D3DXCOLOR di**](d3dxcolor.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che rappresenta il valore di colore negativo del valore del colore.

## <a name="remarks"></a>Commenti

Il canale alfa di input viene copiato, senza modifiche, nel canale alfa di output.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXColorNegative** può essere usata come parametro per un'altra funzione.

Questa funzione restituisce il valore di colore negativo sottraendo 1,0 dai componenti di colore della struttura [**D3DXCOLOR,**](d3dxcolor.md) come illustrato nell'esempio seguente.


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



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

 

 




