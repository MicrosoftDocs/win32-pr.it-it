---
description: Percentuale di tempo di elaborazione dei dati nella pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: D3DDEVINFO_D3D9PIPELINETIMINGS struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d938fd2e1ca0f52d2ea7787f54b430a84907ad5f04f066bc90f0867825745a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676741"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>Struttura D3DDEVINFO \_ D3D9PIPELINETIMINGS

Percentuale di tempo di elaborazione dei dati nella pipeline.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a>Members

<dl> <dt>

**VertexProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato per l'esecuzione di vertex shader.

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato per l'esecuzione di pixel shader.

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato per altre operazioni di elaborazione.

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo in cui non viene elaborata nulla.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per prestazioni ottimali, è consigliabile un carico bilanciato.

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

 

 
