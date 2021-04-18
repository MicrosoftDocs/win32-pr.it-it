---
description: La funzione D3DXBoxBoundProbe (D3DX10math. h) determina se un raggio interseca il volume del rettangolo di delimitazione di una casella.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Funzione D3DXBoxBoundProbe (D3DX10math. h)
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
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334338"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>Funzione D3DXBoxBoundProbe (D3DX10math. h)

Determina se un raggio interseca il volume del rettangolo di delimitazione di una casella.

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

*pMin* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a un [**D3DXVECTOR3**](d3d10-d3dxvector3.md)che descrive l'angolo inferiore sinistro del rettangolo di delimitazione. Vedere la sezione Osservazioni.

</dd> <dt>

*pMax* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive l'angolo superiore destro del rettangolo di delimitazione. Vedere la sezione Osservazioni.

</dd> <dt>

*pRayPosition* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3, che specifica la coordinata di origine del raggio.

</dd> <dt>

*pRayDirection* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore a una struttura D3DXVECTOR3, che specifica la direzione del raggio. Questo vettore non deve essere (0, 0, 0) ma non deve essere normalizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Restituisce **true** se il raggio interseca il volume del rettangolo di delimitazione della casella. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

**D3DXBoxBoundProbe** determina se il raggio interseca il volume del rettangolo di delimitazione della casella, non solo la superficie della casella.

I valori passati a **D3DXBoxBoundProbe** sono xmin, Xmax, ymin, ymax, zmin e Zmax. Pertanto, di seguito vengono definiti gli angoli del rettangolo di delimitazione.


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



La profondità del rettangolo di delimitazione nella direzione z è zmax-zmin, nella direzione y è ymax-ymin e nella direzione x è xmax-xmin. Con i vettori minimi e massimi seguenti, ad esempio, min (-1,-1,-1) e Max (1, 1, 1), il rettangolo di delimitazione viene definito nel modo seguente.


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
| Intestazione  | D3DX10math. h |
| Libreria | D3DX10. lib  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
