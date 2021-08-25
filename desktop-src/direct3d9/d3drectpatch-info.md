---
description: Descrive una patch rettangolare di ordine elevato.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: D3DRECTPATCH_INFO struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b73ebc548031fd931cce0d34edfadf81a73d71d60edf649718875c52cfc992f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850227"
---
# <a name="d3drectpatch_info-structure"></a>Struttura D3DRECTPATCH \_ INFO

Descrive una patch rettangolare di ordine elevato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**StartVertexOffsetWidth**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza iniziale dell'offset dei vertici, in numero di vertici.

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza dell'offset dei vertici iniziale, in numero di vertici.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza di ogni vertice, in numero di vertici.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza di ogni vertice, in numero di vertici.

</dd> <dt>

**Stride**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza della matrice di vertici bidimensionale immaginaria, che occupa lo stesso spazio del buffer dei vertici. Per un esempio, vedere il diagramma seguente.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DBASISTYPE,**](./d3dbasistype.md) che definisce il tipo di base per la patch rettangolare di alto livello.



| Valore                 | Ordine supportato            | Larghezza e altezza                  |
|-----------------------|----------------------------|-----------------------------------|
| BÉZIER D3DBASIS \_      | Lineare, cubica e quintic | Width = height = (DWORD)order + 1 |
| D3DBASIS \_ BSPLINE     | Lineare, cubica e quintic | Width = height > (DWORD)order  |
| INTERPOLAZIONE D3DBASIS \_ | Cubi                      | Width = height > (DWORD)order  |



 

</dd> <dt>

**Gradi**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DDEGREETYPE,**](./d3ddegreetype.md) che definisce il grado per la patch rettangolare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il diagramma seguente identifica i parametri che specificano una patch rettangolare.

![diagramma di una patch rettangolare di ordine elevato e dei parametri che la specificano](images/hop-rectpatch.png)

Ognuno dei vertici nel buffer dei vertici viene visualizzato come punto nero. In questo caso, il buffer dei vertici contiene 20 vertici, di cui 16 nella patch del rettangolo. Lo stride è il numero di vertici nella larghezza del buffer dei vertici, in questo caso cinque. L'offset x per il primo vertice è denominato StartIndexVertexWidth ed è in questo caso 1. L'offset y al primo vertice della patch è denominato StartIndexVertexHeight ed è in questo caso 0.

Per eseguire il rendering di un flusso di singole patch rettangolari (non a mosaico), è necessario interpretare la geometria come una patch rettangolare lunga stretta (1 x N). La **struttura D3DRECTPATCH \_ INFO** per una striscia di questo tipo (Bézier cubica) verrà impostata nel modo seguente.


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
