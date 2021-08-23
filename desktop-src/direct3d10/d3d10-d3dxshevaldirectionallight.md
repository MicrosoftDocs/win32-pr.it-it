---
description: 'Funzione D3DXSHEvalDirectionalLight (D3DX10.h): valuta una luce direzionale e restituisce dati sferici sferici (SH).'
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: Funzione D3DXSHEvalDirectionalLight (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fb50ac274455c67da00d73f91319c0fa17ae85c46f74f4ef605af33e0085ddd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990891"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a>Funzione D3DXSHEvalDirectionalLight (D3DX10.h)

Valuta una luce direzionale e restituisce dati sferici sferici aricali (SH).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
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

Ordine della valutazione SH. Deve essere compreso nell'intervallo da D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

</dd> <dt>

*pDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore al vettore di direzione dell'asse dell'asse dell'emisfero (x, y, z) in cui valutare le funzioni di base sh. Vedere la sezione Osservazioni.

</dd> <dt>

*RIntensity* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Intensità rossa della luce.

</dd> <dt>

*GIntensity* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Intensità verde della luce.

</dd> <dt>

*BIntensity* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Intensità blu della luce.

</dd> <dt>

*pROut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente rosso.

</dd> <dt>

*pGOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore facoltativo al vettore SH di output per il componente verde.

</dd> <dt>

*pBOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore facoltativo al vettore SH di output per il componente blu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Il vettore di output viene calcolato in modo che se il rapporto di intensità R/G/B è uguale a 1, la sorgente di uscita risultante di un punto direttamente sotto la luce su un oggetto diffuso con un albedo pari a 1 sarà 1,0. Verranno calcolati tre esempi spettrali. Verrà restituito pROut, mentre pGOut e pBOut possono essere restituiti.

Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con theta, l'angolo sull'asse z nella direzione a destra e phi, l'angolo da z.

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità. L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.

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

 

 
