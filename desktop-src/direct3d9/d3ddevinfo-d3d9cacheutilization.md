---
description: Misurare le prestazioni della frequenza di riscontri nella cache per trame e vertici indicizzati.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: D3DDEVINFO_D3D9CACHEUTILIZATION struttura (D3D9Types.h)
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
ms.openlocfilehash: 01f0521ca7833cd74c3cb45b5a650fbd12aae485e36a153b57e6d9b10b49d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733072"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>Struttura D3DDEVINFO \_ D3D9CACHEUTILIZATION

Misurare le prestazioni della frequenza di riscontri nella cache per trame e vertici indicizzati.

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Frequenza di riscontri per la ricerca di una trama nella cache delle trame. Si presuppone che sia presente una cache di trame. L'aumento della distorsione del livello di dettaglio per usare la trama più dettagliata, l'uso di molte trame di grandi dimensioni o la produzione di un modello di accesso alla trama quasi casuale su trame di grandi dimensioni con codice shader personalizzato può influire notevolmente sulla frequenza di riscontri nella cache delle trame.

</dd> <dt>

**PostTransformVertexCacheHitRate**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Frequenza di hit per la ricerca dei vertici trasformati nella cache dei vertici. La GPU è progettata per trasformare i vertici indicizzati e può archiviarli in una cache dei vertici. Se si usano mesh, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) o [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) può comportare un migliore utilizzo della cache dei vertici.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una cache efficiente è in genere più vicina a una percentuale di riscontri del 90% e una cache inefficiente è in genere più vicina a una percentuale di riscontri del 10% (anche se una percentuale bassa non è necessariamente un problema).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
