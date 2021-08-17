---
description: Descrive una patch triangolare di ordine elevato.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: D3DTRIPATCH_INFO struttura (D3D9Types.h)
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
ms.openlocfilehash: c20a846d13cd45bb8a1629fca0e958d3042aacf148c24b0633dd19fb5462bd66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850116"
---
# <a name="d3dtripatch_info-structure"></a>Struttura D3DTRIPATCH \_ INFO

Descrive una patch triangolare di ordine elevato.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset iniziale dei vertici, in numero di vertici.

</dd> <dt>

**NumVertices**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di vertici.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DBASISTYPE,**](./d3dbasistype.md) che definisce il tipo di base per la patch triangolare di ordine elevato. L'unico valore valido per questo membro è D3DBASIS \_ BEZIER.

</dd> <dt>

**Gradi**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DDEGREETYPE,**](./d3ddegreetype.md) che definisce il tipo di grado per la patch triangolare di ordine alto.



| Valore                | Numero di vertici |
|----------------------|--------------------|
| CUBO D3DDEGREE \_     | 10                 |
| LINEARE D3DDEGREE \_    | 3                  |
| QUADRATICA D3DDEGREE \_ | N/A                |
| D3DDEGREE \_ QUINTIC   | 21                 |



 

N/D: non disponibile. Non supportata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Ad esempio, il diagramma seguente identifica l'ordine dei vertici e i numeri di segmento per un triangolo di Bézier cubico. L'ordine dei vertici determina i numeri di segmento usati [**da DrawTriPatch.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) L'offset è il numero di byte al primo vertice della patch del triangolo nel vertex buffer.

![diagramma di una patch triangolare di alto ordine con nove vertici](images/hop-tripatch-info.png)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
