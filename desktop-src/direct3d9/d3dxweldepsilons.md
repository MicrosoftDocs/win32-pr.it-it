---
description: 'Struttura D3DXWELDEPSILONS: specifica i valori di tolleranza per ogni componente vertice durante il confronto dei vertici per determinare se sono abbastanza simili da essere uniti.'
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Struttura D3DXWELDEPSILONS (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 63cef1f2023ac29d321775551cdaccd1803c20f76792e0ba9f8136d47782436d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986471"
---
# <a name="d3dxweldepsilons-structure"></a>Struttura D3DXWELDEPSILONS

Specifica i valori di tolleranza per ogni componente vertice durante il confronto dei vertici per determinare se sono abbastanza simili da essere uniti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a>Members

<dl> <dt>

**Position**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Posizione

</dd> <dt>

**BlendWeights**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso blend

</dd> <dt>

**Normal**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Normale

</dd> <dt>

**PSize**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore delle dimensioni in punti

</dd> <dt>

**Speculare**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione speculare

</dd> <dt>

**Diffusa**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Valore di illuminazione diffusa

</dd> <dt>

**Texcoord**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Otto coordinate di trama

</dd> <dt>

**Tangente**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tangente

</dd> <dt>

**Binormale**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Binormale

</dd> <dt>

**TessFactor**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Fattore a tessellazione

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo LPD3DXWELDEPSILONS viene definito come puntatore alla **struttura D3DXWELDEPSILONS.**


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 
