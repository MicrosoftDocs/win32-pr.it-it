---
description: Specifica che il set di istruzioni D3DX è attualmente ottimizzato.
ms.assetid: 5fc97028-4a9d-4bc7-9c90-236a70e570e1
title: D3DX_CPU_OPTIMIZATION enumerazione (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_CPU_OPTIMIZATION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 7bb36b3aeb448933416148b087cb7e82619beef04186637c0bb3fa944a143da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989541"
---
# <a name="d3dx_cpu_optimization-enumeration"></a>Enumerazione DI OTTIMIZZAZIONE CPU D3DX \_ \_

Specifica che il set di istruzioni D3DX è attualmente ottimizzato.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _D3DX_CPU_OPTIMIZATION { 
  D3DX_NOT_OPTIMIZED    = 0,
  D3DX_3DNOW_OPTIMIZED  = 1,
  D3DX_SSE2_OPTIMIZED   = 2,
  D3DX_SSE_OPTIMIZED    = 3
} D3DX_CPU_OPTIMIZATION;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX_NOT_OPTIMIZED"></span><span id="d3dx_not_optimized"></span>**D3DX \_ NON \_ OTTIMIZZATO**
</dt> <dd>

Non ottimizzare.

</dd> <dt>

<span id="D3DX_3DNOW_OPTIMIZED"></span><span id="d3dx_3dnow_optimized"></span>**D3DX \_ 3DNOW \_ OTTIMIZZATO**
</dt> <dd>

Ottimizzare per un 3DNow. set di istruzioni.

</dd> <dt>

<span id="D3DX_SSE2_OPTIMIZED"></span><span id="d3dx_sse2_optimized"></span>**D3DX \_ SSE2 \_ OTTIMIZZATO**
</dt> <dd>

Ottimizzare per un set di istruzioni SSE2.

</dd> <dt>

<span id="D3DX_SSE_OPTIMIZED"></span><span id="d3dx_sse_optimized"></span>**D3DX \_ SSE \_ OTTIMIZZATO**
</dt> <dd>

Ottimizzare per un set di istruzioni SSE.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




