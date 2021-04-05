---
description: Regola il valore di saturazione di un colore.
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: Funzione D3DXColorAdjustSaturation (D3DX10Math. h)
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
ms.openlocfilehash: e6cfa4dd2af6e4a4ac3772af80ba11b8189405f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969456"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>Funzione D3DXColorAdjustSaturation (D3DX10Math. h)

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

*broncio* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Puntatore a un [**D3DXCOLOR**](d3d10-d3dxcolor.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*computer* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Puntatore a una struttura D3DXCOLOR di origine.

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore di saturazione. Questo parametro esegue l'interpolazione lineare tra il colore convertito in scala di grigi e il colore originale, pC. Non sono previsti limiti per il valore di s. Se s è 0, il colore restituito è il colore di scala di grigi. Se s è 1, il colore restituito è il colore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura D3DXCOLOR che è il risultato della regolazione della saturazione.

## <a name="remarks"></a>Commenti

Il canale alfa di input viene copiato, non modificato, nel canale alfa di output.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, questa funzione può essere utilizzata come parametro per un'altra funzione.

Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura D3DXCOLOR tra un colore insaturo e un colore, come illustrato nell'esempio seguente.


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



Se s è maggiore di 0 e minore di 1, la saturazione viene ridotta. Se s è maggiore di 1, la saturazione viene aumentata.

Il colore della scala di grigi viene calcolato come segue:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
