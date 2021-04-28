---
description: 'Funzione D3DXSHEvalDirection (D3DX10.h): valuta le funzioni di base armoniche sferiche (SH) da un vettore di direzione di input.'
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: Funzione D3DXSHEvalDirection (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7fa1f94d65ca8096a0398d71ca2f562b643d47a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108589"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a>Funzione D3DXSHEvalDirection (D3DX10.h)

Valuta le funzioni di base armoniche sferiche (SH) da un vettore di direzione di input.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output armonici sferici (SH). La valutazione genera coefficienti Order². Vedere la sezione Osservazioni.

</dd> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo tra D3DXSH \_ MINORDER e D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Order². Il grado di valutazione è Order - 1.

</dd> <dt>

*pDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Vettore di direzione (x, y, z) in cui valutare le funzioni di base sh. Deve essere normalizzato. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH. Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l I + m + l, dove:

-   l è il grado della funzione di base.
-   m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.

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

 

 
