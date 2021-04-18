---
description: Descrive una patch di ordine superiore rettangolare.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Struttura D3DRECTPATCH_INFO (D3D9Types. h)
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
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322915"
---
# <a name="d3drectpatch_info-structure"></a>Struttura delle informazioni di D3DRECTPATCH \_

Descrive una patch di ordine superiore rettangolare.

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Spessore iniziale dell'offset del vertice, in numero di vertici.

</dd> <dt>

**StartVertexOffsetHeight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza dell'offset del vertice iniziale, in numero di vertici.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza di ogni vertice, in numero di vertici.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza di ogni vertice, in numero di vertici.

</dd> <dt>

**Stride**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza della matrice di vertici bidimensionali immaginaria, che occupa lo stesso spazio del buffer dei vertici. Per un esempio, vedere il diagramma riportato di seguito.

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DBASISTYPE**](./d3dbasistype.md) , che definisce il tipo di base per la patch di ordine superiore rettangolare.



| Valore                 | Ordine supportato            | Larghezza e altezza                  |
|-----------------------|----------------------------|-----------------------------------|
| D3DBASIS \_ Bezier      | Lineare, cubica e Quinta | Width = Height = (DWORD) Order + 1 |
| \_Perequazione BSpline D3DBASIS     | Lineare, cubica e Quinta | Width = ordine altezza > (DWORD)  |
| \_Interpolazione D3DBASIS | Cubi                      | Width = ordine altezza > (DWORD)  |



 

</dd> <dt>

**Gradi**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DDEGREETYPE**](./d3ddegreetype.md) , che definisce il grado per la patch rettangolare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il diagramma seguente identifica i parametri che specificano una patch rettangolo.

![diagramma di una patch di ordine superiore rettangolare e dei parametri che lo specificano](images/hop-rectpatch.png)

Ognuno dei vertici nel buffer del vertice viene visualizzato come un punto nero. In questo caso, il buffer dei vertici contiene 20 vertici, 16 dei quali si trovano nella patch del rettangolo. Lo stride è il numero di vertici nella larghezza del buffer dei vertici, in questo caso cinque. L'offset x al primo vertice è denominato StartIndexVertexWidth ed è in questo caso 1. L'offset y per il primo vertice della patch viene chiamato StartIndexVertexHeight ed è in questo caso 0.

Per eseguire il rendering di un flusso di singole patch rettangolari (non mosaico), è necessario interpretare la geometria come patch rettangolare lunga (1 x N). La struttura delle **\_ informazioni di D3DRECTPATCH** per tale striscia (Bézier cubica) viene configurata nel modo seguente.


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
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**DrawRectPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
