---
description: Definisce i token di monitoraggio del debug.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Enumerazione D3DDEBUGMONITORTOKENS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ed64939714c3ee69fb30e56afe23e52e780405287c898e138ee86822f1c5e0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989071"
---
# <a name="d3ddebugmonitortokens-enumeration"></a>Enumerazione D3DDEBUGMONITORTOKENS

Definisce i token di monitoraggio del debug.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT \_ ENABLE**
</dt> <dd>

Abilitare il monitoraggio del debug.

</dd> <dt>

<span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT \_ DISABLE**
</dt> <dd>

Disabilitare il monitoraggio del debug.

</dd> <dt>

<span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori in questo tipo enumerato vengono usati dallo stato di rendering DEBUGMONITORTOKEN D3DRS e \_ sono rilevanti solo per le build di debug.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
