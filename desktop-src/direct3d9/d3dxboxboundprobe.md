---
description: Determina se un raggio interseca il volume del rettangolo di selezione di un rettangolo.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Funzione D3DXBoxBoundProbe (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 197582c2f404124edd5a49c9d7780ce35cac61b15438a81d120839f283b82373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676391"
---
# <a name="d3dxboxboundprobe-function"></a>Funzione D3DXBoxBoundProbe

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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo inferiore sinistro del rettangolo di selezione. Vedere la sezione Osservazioni.

</dd> <dt>

*pMax* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo superiore destro del rettangolo di selezione. Vedere la sezione Osservazioni.

</dd> <dt>

*pRayPosition* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la coordinata di origine del raggio.

</dd> <dt>

*pRayDirection* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la direzione del raggio. Questo vettore non deve essere (0,0,0), ma non deve essere normalizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Restituisce **TRUE** se il raggio interseca il volume del rettangolo di selezione del rettangolo. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

**D3DXboxBoundProbe** determina se il raggio interseca il volume del rettangolo di selezione del rettangolo, non solo la superficie del rettangolo.

I valori passati **a D3DXboxBoundProbe** sono xmin, xmax, ymin, ymax, zmin e zmax. Di conseguenza, di seguito vengono definiti gli angoli del rettangolo di selezione.


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
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
