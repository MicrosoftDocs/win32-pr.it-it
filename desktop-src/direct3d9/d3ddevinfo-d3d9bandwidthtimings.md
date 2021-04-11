---
description: Metriche della velocità effettiva per informazioni sulla comprensione delle prestazioni di un'applicazione.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Struttura D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
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
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234977"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>\_Struttura D3DDEVINFO D3D9BANDWIDTHTIMINGS

Metriche della velocità effettiva per informazioni sulla comprensione delle prestazioni di un'applicazione.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

La velocità massima di trasferimento dati o la larghezza di banda dalla CPU dell'host alla GPU. Si tratta in genere della larghezza di banda del bus PCI o AGP che connette la CPU e la GPU.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di memoria utilizzata durante il caricamento dei dati dalla CPU dell'host alla GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di velocità effettiva vertice. Questo è il numero di vertici elaborati rispetto alla velocità di elaborazione dei vertici massima teorica.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di velocità effettiva di configurazione del triangolo. Questo è il numero di triangoli configurati per la rasterizzazione rispetto alla velocità di configurazione massima teorica del triangolo.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di velocità effettiva di riempimento pixel. Il numero di pixel compilati rispetto al riempimento teorico dei pixel.

</dd> </dl>

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

 

 
