---
description: Misurare le prestazioni della percentuale di riscontri nella cache per le trame e i vertici indicizzati.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Struttura D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530865"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>\_Struttura D3DDEVINFO D3D9CACHEUTILIZATION

Misurare le prestazioni della percentuale di riscontri nella cache per le trame e i vertici indicizzati.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>Members

<dl> <dt>

**TextureCacheHitRate**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di riscontri per la ricerca di una trama nella cache di trama. Si presuppone che esista una cache di trama. L'aumento della distorsione del livello di dettaglio per usare la trama più dettagliata, l'uso di molte trame di grandi dimensioni o la creazione di un modello di accesso a trama quasi casuale in trame di grandi dimensioni con codice shader personalizzato può influenzare significativamente la percentuale di riscontri nella cache della trama.

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di riscontri per trovare i vertici trasformati nella cache dei vertici. La GPU è progettata per trasformare i vertici indicizzati e può archiviarli in una cache dei vertici. Se si usano mesh, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) o [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) può comportare un migliore utilizzo della cache del vertice.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una cache efficiente è in genere più vicina a una percentuale di riscontri del 90% e una cache inefficiente è in genere più vicina a una percentuale di riscontri del 10% (anche se una percentuale bassa non è necessariamente un problema).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
