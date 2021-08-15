---
description: Ridimensiona un valore di colore.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Funzione D3DXColorScale (D3dx9math.h)
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
ms.openlocfilehash: 95ae2ea24547f566a6da014f408dbfbce5be3112a61688f69e125e91d6085493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241421"
---
# <a name="d3dxcolorscale-function"></a>Funzione D3DXColorScale

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.

</dd> <dt>

*pC* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntatore a una [**struttura D3DXCOLOR di**](d3dxcolor.md) origine.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fattore di scala. Ridimensiona il colore, trattandolo come un vettore 4D. Non sono previsti limiti per il valore di s. Se s è 1, il colore risultante è il colore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che rappresenta il valore del colore ridimensionato.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXColorScale** può essere usata come parametro per un'altra funzione.

Questa funzione calcola il valore del colore ridimensionato moltiplicando i componenti di colore della struttura [**D3DXCOLOR**](d3dxcolor.md) per il fattore di scala specificato, come illustrato nell'esempio seguente.


```
pOut->r = pC->r * s;
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

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> </dl>

 

 
