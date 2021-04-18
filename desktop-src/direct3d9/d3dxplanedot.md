---
description: Calcola il prodotto a punti di un piano e di un vettore 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Funzione D3DXPlaneDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322110"
---
# <a name="d3dxplanedot-function"></a>D3DXPlaneDot (funzione)

Calcola il prodotto a punti di un piano e di un vettore 4D.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PP* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) di origine.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Prodotto a virgola del piano e del vettore 4D.

## <a name="remarks"></a>Commenti

Dato un piano (a, b, c, d) e un vettore 4D (x, y, z, w), il valore restituito di questa funzione è \* x + b \* y + c \* z + d \* . La funzione **D3DXPlaneDot** è utile per determinare la relazione del piano con una coordinata omogenea. Questa funzione, ad esempio, può essere utilizzata per determinare se una coordinata specifica si trova su un particolare piano o su quale lato di un particolare piano si trova una coordinata particolare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
