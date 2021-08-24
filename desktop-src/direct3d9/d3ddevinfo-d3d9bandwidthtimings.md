---
description: Metriche della velocità effettiva per comprendere le prestazioni di un'applicazione.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f9c92a3eae10ef289e53764c7568f826640edf66c3351edaadf3d922515a3eda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565031"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>Struttura D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS

Metriche della velocità effettiva per comprendere le prestazioni di un'applicazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a>Members

<dl> <dt>

**MaxBandwidthUtilized**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza di banda o velocità massima di trasferimento dei dati dalla CPU host alla GPU. Si tratta in genere della larghezza di banda del bus PCI o AGP che connette la CPU e la GPU.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di utilizzo della memoria durante il caricamento dei dati dalla CPU host alla GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di velocità effettiva dei vertici. Si tratta del numero di vertici elaborati rispetto alla velocità di elaborazione massima teorica dei vertici.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di velocità effettiva di configurazione del triangolo. Si tratta del numero di triangoli impostati per la rasterizzazione rispetto alla velocità massima teorica di configurazione del triangolo.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di velocità effettiva di riempimento pixel. Si tratta del numero di pixel riempiti rispetto al riempimento teorico in pixel.

</dd> </dl>

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

 

 
