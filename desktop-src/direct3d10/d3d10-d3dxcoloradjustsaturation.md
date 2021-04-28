---
description: 'Funzione D3DXColorAdjustSaturation (D3DX10Math.h): regola il valore di saturazione di un colore.'
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: Funzione D3DXColorAdjustSaturation (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9e9ae91f5c898dae8ff922616bc02846732c760a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103539"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>Funzione D3DXColorAdjustSaturation (D3DX10Math.h)

Regola il valore di saturazione di un colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Puntatore a [**un oggetto D3DXCOLOR**](d3d10-d3dxcolor.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pC* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Puntatore a una struttura D3DXCOLOR di origine.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore di saturazione. Questo parametro interpola in modo lineare tra il colore convertito in gradazioni di grigio e il colore originale, pC. Non sono previsti limiti al valore di . Se s è 0, il colore restituito è il colore in scala di grigi. Se s è 1, il colore restituito è il colore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura D3DXCOLOR che è il risultato della regolazione della saturazione.

## <a name="remarks"></a>Commenti

Il canale alfa di input viene copiato, senza modifiche, nel canale alfa di output.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, questa funzione può essere usata come parametro per un'altra funzione.

Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura D3DXCOLOR tra un colore non saturo e un colore, come illustrato nell'esempio seguente.


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



Se s è maggiore di 0 e minore di 1, la saturazione viene ridotta. Se s è maggiore di 1, la saturazione viene aumentata.

Il colore in scala di grigi viene calcolato come:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
