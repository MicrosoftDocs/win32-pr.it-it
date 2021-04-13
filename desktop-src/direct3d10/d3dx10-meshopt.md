---
description: Specifica il tipo di ottimizzazione mesh da eseguire.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Enumerazione D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: c8ccb13da1549b7e2eeeb67ebf7899c2187be363
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355559"
---
# <a name="d3dx10_meshopt-enumeration"></a>\_Enumerazione d3dx10 MESHOPT

Specifica il tipo di ottimizzazione mesh da eseguire.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ Compact**
</dt> <dd>

Riordina i visi per rimuovere i vertici e i visi inutilizzati.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ attr \_ Sort**
</dt> <dd>

Riordina i visi per ottimizzare le modifiche dello stato del bundle di attributi e le prestazioni DrawSubset migliorate.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ Vertex \_ cache**
</dt> <dd>

Riordina i visi per aumentare la percentuale di riscontri nella cache delle cache dei vertici.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**Riordino della \_ striscia MESHOPT d3dx10 \_ \_**
</dt> <dd>

Riordina i visi per ottimizzare la lunghezza dei triangoli adiacenti.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ Ignora i \_ vertici**
</dt> <dd>

Ottimizza solo le facce; non ottimizzare i vertici.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**\_MESHOPT d3dx10 \_ \_ non \_ suddivise**
</dt> <dd>

Durante l'ordinamento degli attributi, non suddividere i vertici condivisi tra gruppi di attributi.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ dispositivo \_ indipendente**
</dt> <dd>

Influiscono sulle dimensioni della cache dei vertici. L'uso di questo flag specifica una dimensione predefinita della cache Vertex che funziona correttamente nell'hardware legacy.

</dd> </dl>

## <a name="remarks"></a>Commenti

I \_ flag di ottimizzazione D3DXMESHOPT STRIPREORDER e D3DXMESHOPT \_ VERTEXCACHE si escludono a vicenda.

Il \_ flag SHAREVB di D3DXMESHOPT è stato rimosso da questa enumerazione. Usare \_ invece D3DXMESH VB \_ share, in D3DXMESH.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




