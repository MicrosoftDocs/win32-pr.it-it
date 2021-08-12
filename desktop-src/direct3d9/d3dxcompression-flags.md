---
description: Definisce la modalità di compressione usata per l'archiviazione dei dati dei set di animazioni compressi.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: D3DXCOMPRESSION_FLAGS enumerazione (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: a4d1e19e2e6fb8e0625b20c7755b3cf3b5c68c06cbc01da1b8a22fd9893d0027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299999"
---
# <a name="d3dxcompression_flags-enumeration"></a>Enumerazione D3DXCOMPRESSION \_ FLAGS

Definisce la modalità di compressione usata per l'archiviazione dei dati dei set di animazioni compressi.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ DEFAULT**
</dt> <dd>

Implementa la compressione rapida.

</dd> <dt>

<span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ STRONG**
</dt> <dd>

Implementa la compressione lenta. In genere, viene restituito un set di animazioni compresse di migliore qualità rispetto all'uso di D3DXCOMPRESS \_ DEFAULT.

</dd> <dt>

<span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




