---
description: Percentuale del tempo di elaborazione dei dati nella pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: Struttura D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types. h)
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
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322405"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>\_Struttura D3DDEVINFO D3D9PIPELINETIMINGS

Percentuale del tempo di elaborazione dei dati nella pipeline.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato per l'esecuzione di vertex shader.

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato per l'esecuzione di pixel shader.

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale di tempo impiegato per eseguire altre operazioni di elaborazione.

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentuale del tempo che non elabora alcun elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ottenere prestazioni ottimali, è consigliabile un carico bilanciato.

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

 

 
