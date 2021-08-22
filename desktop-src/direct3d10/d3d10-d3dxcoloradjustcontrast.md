---
description: 'Funzione D3DXColorAdjustContrast (D3DX10Math.h): regola il valore di contrasto di un colore.'
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: Funzione D3DXColorAdjustContrast (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 90c36ee9c414b6ae34058b255ad2e7a642f13ef49ee91b586ca974009d4e6b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498491"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a>Funzione D3DXColorAdjustContrast (D3DX10Math.h)

Regola il valore di contrasto di un colore.

## <a name="syntax"></a>Sintassi


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

\[in, out \] Puntatore a [**un oggetto D3DXCOLOR**](d3d10-d3dxcolor.md) che è il risultato dell'operazione.

</dd> <dt>

*pC* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Puntatore a una struttura D3DXCOLOR di origine.

</dd> <dt>

*c* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore di contrasto. Questo parametro interpola in modo lineare tra la percentuale di grigio e il colore pC. Non sono previsti limiti al valore di c. Se questo parametro è zero, il colore restituito è la percentuale di grigio. Se questo parametro è 1, il colore restituito è il colore originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Questa funzione restituisce un puntatore a una struttura D3DXCOLOR che è il risultato della regolazione del contrasto.

## <a name="remarks"></a>Commenti

Il canale alfa di input viene copiato, senza modifiche, nel canale alfa di output.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, questa funzione può essere usata come parametro per un'altra funzione.

Questa funzione interpola i componenti di colore rosso, verde e blu di una struttura D3DXCOLOR tra la percentuale di grigio e un valore di contrasto specificato, come illustrato nell'esempio seguente.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Se c è maggiore di 0 e minore di 1, il contrasto viene ridotto. Se c è maggiore di 1, il contrasto viene aumentato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
