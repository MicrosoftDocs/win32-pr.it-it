---
description: Ridimensiona un valore di colore.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Funzione D3DXColorScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323012"
---
# <a name="d3dxcolorscale-function"></a>D3DXColorScale (funzione)

Ridimensiona un valore di colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
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

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di scala. Ridimensiona il colore, considerandolo come un vettore 4D. Non sono previsti limiti per il valore di s. Se s è 1, il colore risultante è quello originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che corrisponde al valore di colore ridimensionato.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXColorScale** può essere utilizzata come parametro per un'altra funzione.

Questa funzione calcola il valore del colore scalato moltiplicando i componenti del colore della struttura [**D3DXCOLOR**](d3dxcolor.md) in base al fattore di scala specificato, come illustrato nell'esempio seguente.


```
pOut->r = pC->r * s;
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

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> </dl>

 

 
