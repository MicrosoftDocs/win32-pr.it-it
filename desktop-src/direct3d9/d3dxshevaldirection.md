---
description: 'Funzione D3DXSHEvalDirection (D3dx9math.h): valuta le funzioni di base sferiche ariche (SH) da un vettore di direzione di input.'
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: Funzione D3DXSHEvalDirection (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16b2d75c885a2d5328b9a11ff9c8924ad78bf3e514e5b5696397625b5b080529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676081"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a>Funzione D3DXSHEvalDirection (D3dx9math.h)

Valuta le funzioni di base sferiche aricali (SH) da un vettore di direzione di input.

## <a name="syntax"></a>Sintassi


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output sferici aricali (SH). La valutazione genera coefficienti Di ordine. Vedere la sezione Osservazioni.

</dd> <dt>

*Ordine* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordine della valutazione SH. Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi. La valutazione genera coefficienti Di ordine. Il grado di valutazione è Order - 1.

</dd> <dt>

*pDir* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Vettore di direzione (x, y, z) in cui valutare le funzioni di base sh. Deve essere normalizzato. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntatore ai coefficienti di output SH. Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria lÊ + m + l, dove:

-   l è il grado della funzione di base.
-   m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.

Sulla sfera con raggio dell'unità, come illustrato nella figura seguente, la direzione può essere specificata [](coordinate-systems.md)semplicemente con theta, l'angolo verso l'asse z nella direzione a destra e phi, l'angolo da z.

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

 

 
