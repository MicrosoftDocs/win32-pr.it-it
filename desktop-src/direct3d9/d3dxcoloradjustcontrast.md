---
description: Regola il valore di contrasto di un colore.
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: Funzione D3DXColorAdjustContrast (D3dx9math. h)
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
ms.openlocfilehash: c6765f442b6a2550ba262073f61c876e3b3ae1fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322882"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a>Funzione D3DXColorAdjustContrast (D3dx9math. h)

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

*c* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore di contrasto. Questo parametro esegue l'interpolazione lineare tra il 50% di grigio e il colore, pC. Non sono previsti limiti per il valore di c. Se questo parametro è zero, il colore restituito è il 50% di grigio. Se questo parametro è 1, il colore restituito è quello originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato della regolazione del contrasto.

## <a name="remarks"></a>Commenti

Il canale alfa di input viene copiato, non modificato, nel canale alfa di output.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, questa funzione può essere utilizzata come parametro per un'altra funzione.

Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura [**D3DXCOLOR**](d3dxcolor.md) tra il 50% di grigio e un valore di contrasto specificato, come illustrato nell'esempio seguente.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Se c è maggiore di 0 e minore di 1, il contrasto viene ridotto. Se c è maggiore di 1, il contrasto viene aumentato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustSaturation**](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
