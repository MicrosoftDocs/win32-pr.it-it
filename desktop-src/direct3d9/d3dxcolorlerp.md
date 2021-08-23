---
description: Usa l'interpolazione lineare per creare un valore di colore.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Funzione D3DXColorLerp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa0134ca1c3cf88e0e25f253cca4ebeb16a89b5bdaa982cf4e9e96e85bfb1d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988701"
---
# <a name="d3dxcolorlerp-function"></a>Funzione D3DXColorLerp

Usa l'interpolazione lineare per creare un valore di colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pC1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntatore a una [**struttura D3DXCOLOR di**](d3dxcolor.md) origine.

</dd> <dt>

*pC2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Puntatore a una [**struttura D3DXCOLOR di**](d3dxcolor.md) origine.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parametro che interpola in modo lineare tra i colori, pC1 e pC2, trattandoli entrambi come vettori 4D. Non sono previsti limiti al valore di .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'interpolazione lineare.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXColorLerp** può essere usata come parametro per un'altra funzione.

Questa funzione interpola i componenti rosso, verde, blu e alfa di una struttura [**D3DXCOLOR**](d3dxcolor.md) tra due colori, come illustrato nell'esempio seguente.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Se si interpola in modo lineare tra i colori A e B e s è 0, il colore risultante è A. Se s è 1, il colore risultante è il colore B.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
