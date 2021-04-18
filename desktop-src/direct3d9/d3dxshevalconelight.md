---
description: Valuta una luce che è un cono di intensità costante e restituisce dati SH (spettrale sferici).
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: Funzione D3DXSHEvalConeLight (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2400fe0430e008ea1b704ee4daef51eeee7bd7a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104553162"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a>Funzione D3DXSHEvalConeLight (D3dx9math. h)

Valuta una luce che è un cono di intensità costante e restituisce dati SH (spettrale sferici).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*pDir* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore al vettore di direzione dell'asse del (x, y, z) in cui valutare le funzioni di base SH. Vedere la sezione Osservazioni.

</dd> <dt>

*Raggio* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Raggio di cono in radianti.

</dd> <dt>

*RIntensity* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Intensità rossa della luce.

</dd> <dt>

*GIntensity* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Intensità verde della luce.

</dd> <dt>

*BIntensity* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Intensità blu della luce.

</dd> <dt>

*pROut* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente rosso.

</dd> <dt>

*pGOut* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente verde.

</dd> <dt>

*pBOut* \[ out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente blu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Valuta una luce che è un cono di intensità costante e restituisce dati SH spettrali. Il vettore di output viene calcolato in modo tale che se il rapporto di intensità R/G/B è uguale a 1, la luminosità di uscita di un punto immediatamente sotto la luce (orientata alla direzione del cono su un oggetto diffuso con un'albedo pari a 1) è 1,0. Verrà calcolato tre campioni spettrali; viene restituito *pROut* , mentre *pGOut* e *pBOut* possono essere restituiti.

Nella sfera con raggio di unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con Theta, l'angolo sull'asse z nella [direzione destra](coordinate-systems.md)e Phi, l'angolo da z.

![illustrazione di una sfera con raggio unitario](images/spherical-coordinates.png)

Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, Phi) nella sfera dell'unità. L'angolo theta varia nell'intervallo compreso tra 0 e 2 pi, mentre Phi varia da 0 a pi.

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Trasferimento Radiance pre-calcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
