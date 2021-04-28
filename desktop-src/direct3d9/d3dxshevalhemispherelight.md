---
description: "Funzione D3DXSHEvalHemisphereLight (D3dx9math.h): valuta una luce che è un'interpolazione lineare tra due colori sulla sfera."
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: Funzione D3DXSHEvalHemisphereLight (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc06dcf866c21cc5dcb96b23dea5a4640293fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093967"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a>Funzione D3DXSHEvalHemisphereLight (D3dx9math.h)

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

Ordine della valutazione armonica sferica (SH). Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Order². Il grado di valutazione è Order - 1.

</dd> <dt>

*pDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore al vettore di direzione dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base sh. Vedere la sezione Osservazioni.

</dd> <dt>

*In alto* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**

Colore del cielo.

</dd> <dt>

*In basso* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**

Colore del suolo.

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

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

L'interpolazione viene eseguita in modo lineare tra i due punti, non sulla superficie della sfera ,ovvero se l'asse è (0,0,1) è lineare in Z, non nell'angolo azimutabile. La funzione di illuminazione sferica risultante viene normalizzata in modo che un punto su una superficie perfettamente diffusa senza ombreggiatura e un normale puntato nella direzione *pDir* comporterebbe la luminosità di uscita con un valore pari a 1 (se il colore superiore era bianco e il colore inferiore era nero). Si tratta di un modello molto semplice in cui *Top* rappresenta l'intensità del "cielo" e *Bottom* rappresenta l'intensità del "terreno".

Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente [](coordinate-systems.md)con theta, l'angolo sull'asse z nella direzione a destra e phi, l'angolo da z.

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità. L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Trasferimento di radiance pre-ricalcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
