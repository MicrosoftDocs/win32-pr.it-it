---
description: La funzione D3DXBoxBoundProbe (D3DX10math.h) determina se un raggio interseca il volume del rettangolo di selezione di un rettangolo.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Funzione D3DXBoxBoundProbe (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae06fa2e42e99dc64a0684844e341f26e30d797e75d3a822aa0b1ddee690703d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028811"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>Funzione D3DXBoxBoundProbe (D3DX10math.h)

Determina se un raggio interseca il volume del rettangolo di selezione di un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMin* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a [**un oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md)che descrive l'angolo inferiore sinistro del rettangolo di selezione. Vedere la sezione Osservazioni.

</dd> <dt>

*pMax* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive l'angolo superiore destro del rettangolo di selezione. Vedere la sezione Osservazioni.

</dd> <dt>

*pRayPosition* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3, che specifica la coordinata di origine del raggio.

</dd> <dt>

*pRayDirection* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3, che specifica la direzione del raggio. Questo vettore non deve essere (0,0,0), ma non deve essere normalizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Restituisce **TRUE** se il raggio interseca il volume del rettangolo di selezione del rettangolo. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

**D3DXBoxBoundProbe** determina se il raggio interseca il volume del rettangolo di selezione del rettangolo, non solo la superficie del rettangolo.

I valori passati **a D3DXBoxBoundProbe** sono xmin, xmax, ymin, ymax, zmin e zmax. Di conseguenza, di seguito vengono definiti gli angoli del rettangolo di selezione.


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



La profondità del rettangolo di selezione nella direzione z è zmax - zmin, nella direzione y è ymax - ymin e nella direzione x è xmax - xmin. Ad esempio, con i vettori minimo e massimo seguenti, min (-1, -1, -1) e max (1, 1, 1), il rettangolo di selezione viene definito nel modo seguente.


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione  | D3DX10math.h |
| Libreria | D3DX10.lib  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
