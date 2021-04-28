---
description: 'Funzione D3DXColorAdjustContrast (D3dx9math.h): regola il valore di contrasto di un colore.'
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: Funzione D3DXColorAdjustContrast (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115879"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a>Funzione D3DXColorAdjustContrast (D3dx9math.h)

Regola il valore di contrasto di un colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
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

</dd> <dt>

*c* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore di contrasto. Questo parametro interpola in modo lineare tra il 50% di grigio e il colore, pC. Non sono previsti limiti per il valore di c. Se questo parametro è zero, il colore restituito è il 50% grigio. Se questo parametro è 1, il colore restituito è il colore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a [**una struttura D3DXCOLOR**](d3dxcolor.md) che è il risultato della regolazione del contrasto.

## <a name="remarks"></a>Commenti

Il canale alfa di input viene copiato, senza modifiche, nel canale alfa di output.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, questa funzione può essere usata come parametro per un'altra funzione.

Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura [**D3DXCOLOR**](d3dxcolor.md) tra la percentuale di grigio e un valore di contrasto specificato, come illustrato nell'esempio seguente.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Se c è maggiore di 0 e minore di 1, il contrasto viene ridotto. Se c è maggiore di 1, il contrasto viene aumentato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustSaturation**](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
