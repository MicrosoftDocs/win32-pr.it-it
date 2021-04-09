---
description: Usa l'interpolazione lineare per creare un valore di colore.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Funzione D3DXColorLerp (D3dx9math. h)
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
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886291"
---
# <a name="d3dxcolorlerp-function"></a>D3DXColorLerp (funzione)

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

</dd> <dt>

*s* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Parametro che esegue l'interpolazione lineare tra i colori, pC1 e pC2, considerandoli entrambi come vettori 4D. Non sono previsti limiti per il valore di s.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'interpolazione lineare.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione **D3DXColorLerp** può essere utilizzata come parametro per un'altra funzione.

Questa funzione esegue l'interpolazione dei componenti rosso, verde, blu e alfa di una struttura [**D3DXCOLOR**](d3dxcolor.md) tra due colori, come illustrato nell'esempio seguente.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Se si esegue l'interpolazione lineare tra i colori A e B e s è 0, il colore risultante è un. Se s è 1, il colore risultante è il colore B.

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

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
