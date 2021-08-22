---
description: Definisce le operazioni stencil-buffer.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumerazione D3DSTENCILOP (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 166f670e6e34edd6a3b05584c54e63be274e54161faea242fa701e771a90a771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564941"
---
# <a name="d3dstencilop-enumeration"></a>Enumerazione D3DSTENCILOP

Definisce le operazioni stencil-buffer.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ KEEP**
</dt> <dd>

Non aggiornare la voce nel buffer degli stencil. Si tratta del valore predefinito.

</dd> <dt>

<span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ ZERO**
</dt> <dd>

Impostare la voce stencil-buffer su 0.

</dd> <dt>

<span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ REPLACE**
</dt> <dd>

Sostituire la voce stencil-buffer con un valore di riferimento.

</dd> <dt>

<span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**
</dt> <dd>

Incrementare la voce stencil-buffer, fissando al valore massimo.

</dd> <dt>

<span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**
</dt> <dd>

Decrementare la voce stencil-buffer, fissando a zero.

</dd> <dt>

<span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ INVERT**
</dt> <dd>

Invertire i bit nella voce stencil-buffer.

</dd> <dt>

<span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ INCR**
</dt> <dd>

Incrementare la voce stencil-buffer, a capo su zero se il nuovo valore supera il valore massimo.

</dd> <dt>

<span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**DECREMENTO D3DSTENCILOP \_**
</dt> <dd>

Decrementare la voce stencil-buffer, a capo fino al valore massimo se il nuovo valore è minore di zero.

</dd> <dt>

<span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le voci stencil-buffer sono valori interi compresi tra 0 e 2ⁿ - 1, dove n è la profondità in bit del buffer degli stencil.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




