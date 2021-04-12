---
description: Valuta una luce che rappresenta un'interpolazione lineare tra due colori sulla sfera.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Funzione D3DXSHEvalHemisphereLight (D3DX10. h)
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
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355324"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a>Funzione D3DXSHEvalHemisphereLight (D3DX10. h)

Valuta una luce che rappresenta un'interpolazione lineare tra due colori sulla sfera.

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

*Ordine* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordine della valutazione dell'armonica sferica (SH). Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi. La valutazione genera coefficienti Order ². Il livello della valutazione è Order-1.

</dd> <dt>

*pDir* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore al vettore di direzione dell'asse del (x, y, z) in cui valutare le funzioni di base SH. Vedere la sezione Osservazioni.

</dd> <dt>

In *alto* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Colore celeste.

</dd> <dt>

In *basso* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Colore di base.

</dd> <dt>

*pROut* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente rosso.

</dd> <dt>

*pGOut* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente verde.

</dd> <dt>

*pBOut* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al vettore SH di output per il componente blu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

L'interpolazione viene eseguita in modo lineare tra i due punti, non sulla superficie della sfera (ovvero se l'asse è (0, 0, 1) è lineare in Z, non nell'angolo azimutale). La funzione di illuminazione sferica risultante viene normalizzata in modo che un punto su una superficie perfettamente diffusa senza ombreggiatura e un normale punto nella direzione pDir comporti la radianza di uscita con un valore pari a 1 (se il colore superiore era bianco e il colore inferiore era nero). Si tratta di un modello molto semplice in cui top rappresenta l'intensità del "cielo" e della parte inferiore rappresenta l'intensità della "superficie".

Nella sfera con raggio di unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con Theta, l'angolo sull'asse z nella direzione destra e Phi, l'angolo da z.

![illustrazione di una sfera con raggio unitario](images/spherical-coordinates.png)

Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, Phi) nella sfera dell'unità. L'angolo theta varia nell'intervallo compreso tra 0 e 2 pi, mentre Phi varia da 0 a pi.

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
