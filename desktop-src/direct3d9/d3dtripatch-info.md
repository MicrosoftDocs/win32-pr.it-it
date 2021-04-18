---
description: Descrive una patch di ordine superiore triangolare.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Struttura D3DTRIPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323260"
---
# <a name="d3dtripatch_info-structure"></a>Struttura delle informazioni di D3DTRIPATCH \_

Descrive una patch di ordine superiore triangolare.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**StartVertexOffset**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset del vertice iniziale, in numero di vertici.

</dd> <dt>

**NumVertices**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di vertici.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DBASISTYPE**](./d3dbasistype.md) , che definisce il tipo di base per la patch di ordine superiore triangolare. L'unico valore valido per questo membro è D3DBASIS \_ Bezier.

</dd> <dt>

**Gradi**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DDEGREETYPE**](./d3ddegreetype.md) , che definisce il tipo di grado per la patch di ordine superiore triangolare.



| Valore                | Numero di vertici |
|----------------------|--------------------|
| \_Cubi D3DDEGREE     | 10                 |
| D3DDEGREE \_ lineare    | 3                  |
| D3DDEGREE \_ quadratico | N/D                |
| D3DDEGREE \_ quinte   | 21                 |



 

N/A: non disponibile. Non supportata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il diagramma seguente, ad esempio, identifica i numeri di ordine e di segmento dei vertici per una patch del triangolo di Bézier cubica. L'ordine dei vertici determina i numeri di segmento usati da [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch). L'offset è il numero di byte al primo vertice della patch del triangolo nel buffer dei vertici.

![diagramma di una patch di ordine superiore triangolare con nove vertici](images/hop-tripatch-info.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
