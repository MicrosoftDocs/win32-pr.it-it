---
description: "Funzione D3DXSHEvalHemisphereLight (D3DX10.h): valuta una luce che è un'interpolazione lineare tra due colori sulla sfera."
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Funzione D3DXSHEvalHemisphereLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 355dae7b843d5acfbb842b7bd08c329bdaed4306
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108569"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a>Funzione D3DXSHEvalHemisphereLight (D3DX10.h)

Valuta una luce che è un'interpolazione lineare tra due colori sulla sfera.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione sferica aricale (SH). Deve essere compreso nell'intervallo da D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

</dd> <dt>

*pDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore al vettore di direzione dell'asse dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base sh. Vedere la sezione Osservazioni.

</dd> <dt>

*In alto* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Colore del cielo.

</dd> <dt>

*In basso* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Colore del terreno.

</dd> <dt>

*pROut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente rosso.

</dd> <dt>

*pGOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente verde.

</dd> <dt>

*pBOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente blu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

L'interpolazione viene eseguita in modo lineare tra i due punti, non sulla superficie della sfera ,ovvero se l'asse è (0,0,1) è lineare in Z, non nell'angolo azimuthal. La funzione di illuminazione sferica risultante viene normalizzata in modo che un punto su una superficie perfettamente diffusa senza ombreggiatura e un normale puntato nella direzione pDir comporterebbe una luminosità di uscita con valore 1 (se il colore superiore era bianco e il colore inferiore era nero). Si tratta di un modello molto semplice in cui Top rappresenta l'intensità del "cielo" e Bottom rappresenta l'intensità del "terreno".

Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con theta, l'angolo circa l'asse z nella direzione destra e phi, l'angolo da z.

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

Le equazioni seguenti mostrano la relazione tra coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità. L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
