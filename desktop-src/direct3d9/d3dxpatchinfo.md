---
description: Struttura che contiene gli attributi di una mesh di patch.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Struttura D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354144"
---
# <a name="d3dxpatchinfo-structure"></a>Struttura D3DXPATCHINFO

Struttura che contiene gli attributi di una mesh di patch.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**PatchType**
</dt> <dd>

Tipo: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**

</dd> <dd>

Tipo di patch. Per informazioni sui tipi di patch, vedere [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).

</dd> <dt>

**Gradi**
</dt> <dd>

Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**

</dd> <dd>

Grado delle curve usate per costruire la patch. Per informazioni sui gradi supportati, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

**Basis**
</dt> <dd>

Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**

</dd> <dd>

Tipo di curva utilizzata per costruire la patch. Per informazioni sui tipi di base supportati, vedere [**D3DBASISTYPE**](./d3dbasistype.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Una mesh è un set di visi, ciascuno dei quali è descritto da un semplice poligono. È possibile creare oggetti connettendosi tra loro diverse mesh. Una mesh patch viene costruita dalle patch. Una patch è una parte di geometria a quattro lati costruita dalle curve. Il tipo di curva usato e l'ordine della curva possono essere variati in modo che l'area della patch possa adattarsi quasi a qualsiasi forma di superficie.

Sono supportati i tipi di combinazioni di patch seguenti:



| Tipo di patch | Base       | Gradi |
|------------|-------------|--------|
| Rettangolo  | Bézier      | 2, 3, 5  |
| Rettangolo  | Spline B    | 2, 3, 5  |
| Rettangolo  | Catmull-Rom | 3      |
| Triangle   | Bézier      | 2, 3, 5  |
| N-patch    | N/D         | 3      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**\_Informazioni D3DRECTPATCH**](d3drectpatch-info.md)
</dt> <dt>

[**\_Informazioni D3DTRIPATCH**](d3dtripatch-info.md)
</dt> <dt>

[**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
