---
description: Definisce le operazioni del buffer di stencil.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumerazione D3DSTENCILOP (D3D9Types. h)
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
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322439"
---
# <a name="d3dstencilop-enumeration"></a>Enumerazione D3DSTENCILOP

Definisce le operazioni del buffer di stencil.

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

<span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ Keep**
</dt> <dd>

Non aggiornare la voce nel buffer dello stencil. Si tratta del valore predefinito.

</dd> <dt>

<span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ zero**
</dt> <dd>

Impostare la voce stencil-buffer su 0.

</dd> <dt>

<span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ Sostituisci**
</dt> <dd>

Sostituire la voce dello stencil buffer con un valore di riferimento.

</dd> <dt>

<span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**\_INCRSAT D3DSTENCILOP**
</dt> <dd>

Incrementa la voce dello stencil buffer, bloccando il valore massimo.

</dd> <dt>

<span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**\_DECRSAT D3DSTENCILOP**
</dt> <dd>

Decrementa la voce del buffer di stencil, che viene fissata a zero.

</dd> <dt>

<span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP \_ invertito**
</dt> <dd>

Inverti i bit nella voce dello stencil buffer.

</dd> <dt>

<span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**\_Incr D3DSTENCILOP**
</dt> <dd>

Incrementa la voce dello stencil buffer, eseguendo il wrapping su zero se il nuovo valore supera il valore massimo.

</dd> <dt>

<span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**\_Decr D3DSTENCILOP**
</dt> <dd>

Decrementa la voce dello stencil buffer, eseguendo il wrapping fino al valore massimo se il nuovo valore è minore di zero.

</dd> <dt>

<span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli stencil: le voci del buffer sono valori integer compresi tra 0 e 2 Grigioni-1, dove n è la profondità di bit del buffer dello stencil.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




