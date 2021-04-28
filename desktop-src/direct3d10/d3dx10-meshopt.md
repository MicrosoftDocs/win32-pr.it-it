---
description: 'D3DX10_MESHOPT enumerazione : specifica il tipo di ottimizzazione mesh da eseguire.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT enumerazione (D3DX10Mesh.h)
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
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105449"
---
# <a name="d3dx10_meshopt-enumeration"></a>Enumerazione D3DX10 \_ MESHOPT

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

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**
</dt> <dd>

Riordina i visi per rimuovere i vertici e i visi inutilizzati.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ SORT**
</dt> <dd>

Riordina i visi per ottimizzare un minor numero di modifiche dello stato di aggregazione degli attributi e migliorare le prestazioni di DrawSubset.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ VERTEX \_ CACHE**
</dt> <dd>

Riordina i visi per aumentare la frequenza di riscontri nella cache delle cache dei vertici.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10 \_ MESHOPT \_ STRIP \_ REORDER**
</dt> <dd>

Riordina i visi per ottimizzare la lunghezza dei triangoli adiacenti.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ IGNORE \_ VERTS**
</dt> <dd>

Ottimizzare solo i visi; non ottimizzare i vertici.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ NON \_ \_ SUDDIVISO**
</dt> <dd>

Durante l'ordinamento degli attributi, non suddividere i vertici condivisi tra gruppi di attributi.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ DEVICE \_ INDEPENDENT**
</dt> <dd>

Influisce sulle dimensioni della cache dei vertici. L'uso di questo flag specifica una dimensione predefinita della cache dei vertici che funziona bene nell'hardware legacy.

</dd> </dl>

## <a name="remarks"></a>Commenti

I flag di ottimizzazione \_ VERTEXCACHE D3DXMESHOPT STRIPREORDER e D3DXMESHOPT si \_ escludono a vicenda.

Il flag D3DXMESHOPT \_ SHAREVB è stato rimosso da questa enumerazione. Usare D3DXMESH \_ VB \_ SHARE in D3DXMESH.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




