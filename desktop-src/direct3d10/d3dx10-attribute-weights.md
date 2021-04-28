---
description: 'D3DX10_ATTRIBUTE_WEIGHTS struttura : specifica gli attributi di spessore della mesh.'
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: D3DX10_ATTRIBUTE_WEIGHTS (D3DX10.h)
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
ms.openlocfilehash: ab163149493ad73f892a251a691ad82544d7f382
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094354"
---
# <a name="d3dx10_attribute_weights-structure"></a>Struttura WEIGHTS DEGLI ATTRIBUTI D3DX10 \_ \_

Specifica gli attributi di spessore della mesh.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione.

</dd> <dt>

**Limite**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Spessore blend.

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Normale.

</dd> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione diffusa.

</dd> <dt>

**Speculare**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione speculare.

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Otto coordinate di trama.

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente.

</dd> <dt>

**Binormale**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormale.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura descrive in che modo un'operazione di semplificazione considererà i dati dei vertici durante il calcolo dei costi relativi tra i bordi di compressione. Ad esempio, se il campo Normale è 0,0, l'operazione di semplificazione ignorerà il componente normale del vertice durante il calcolo dell'errore per la compressione. Tuttavia, se il campo Normal è 1.0, l'operazione di semplificazione userà il componente normale dei vertici. Se il campo Normale è 2.0, raddoppiare la quantità di errori. se il campo Normale è 4.0, quindi quadruplicare il numero di errori e così via.

Il tipo WEIGHTS ATTRIBUTE LPD3DX è definito come puntatore alla struttura \_ \_ ATTRIBUTE WEIGHTS D3DX. \_ \_


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
