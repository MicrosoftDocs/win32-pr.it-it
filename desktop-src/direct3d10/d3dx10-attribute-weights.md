---
description: Specifica gli attributi di peso mesh.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Struttura D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355109"
---
# <a name="d3dx10_attribute_weights-structure"></a>\_ \_ Struttura weights dell'attributo d3dx10

Specifica gli attributi di peso mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a>Members

<dl> <dt>

**Position**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione.

</dd> <dt>

**Limite**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Spessore di Blend.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Normale.

</dd> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione diffuso.

</dd> <dt>

**Speculare**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione speculare.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Otto coordinate di trama.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormale**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura descrive il modo in cui un'operazione di semplificazione considererà i dati dei vertici quando si calcolano i costi relativi tra i bordi. Se, ad esempio, il campo normale è 0,0, l'operazione di semplificazione ignorerà il componente normale vertice durante il calcolo dell'errore per la compressione. Tuttavia, se il campo normale è 1,0, l'operazione di semplificazione utilizzerà il componente normale vertice. Se il campo normale è 2,0, raddoppiare la quantità di errori; Se il campo normale è 4,0, moltiplicare il numero di errori e così via.

Il \_ \_ tipo di ponderazione dell'attributo LPD3DX è definito come un puntatore alla \_ struttura dell'attributo D3DX \_ weights.


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
