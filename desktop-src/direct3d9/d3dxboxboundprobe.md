---
description: Determina se un raggio interseca il volume del rettangolo di delimitazione di una casella.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Funzione D3DXBoxBoundProbe (D3DX9Mesh. h)
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
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132354"
---
# <a name="d3dxboxboundprobe-function"></a>D3DXBoxBoundProbe (funzione)

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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo inferiore sinistro del rettangolo di delimitazione. Vedere la sezione Osservazioni.

</dd> <dt>

*pMax* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo superiore destro del rettangolo di delimitazione. Vedere la sezione Osservazioni.

</dd> <dt>

*pRayPosition* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la coordinata di origine del raggio.

</dd> <dt>

*pRayDirection* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) , che specifica la direzione del raggio. Questo vettore non deve essere (0, 0, 0) ma non deve essere normalizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Restituisce **true** se il raggio interseca il volume del rettangolo di delimitazione della casella. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

**D3DXboxBoundProbe** determina se il raggio interseca il volume del rettangolo di delimitazione della casella, non solo la superficie della casella.

I valori passati a **D3DXboxBoundProbe** sono xmin, Xmax, ymin, ymax, zmin e Zmax. Pertanto, di seguito vengono definiti gli angoli del rettangolo di delimitazione.


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
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
