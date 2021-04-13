---
description: Descrive il tipo di eventi che possono essere codificati dal controller animazione.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: Enumerazione D3DXEVENT_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354879"
---
# <a name="d3dxevent_type-enumeration"></a>\_Enumerazione del tipo D3DXEVENT

Descrive il tipo di eventi che possono essere codificati dal controller animazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**\_TRACKSPEED D3DXEVENT**
</dt> <dd>

Rileva velocità.

</dd> <dt>

<span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**\_TRACKWEIGHT D3DXEVENT**
</dt> <dd>

Tenere traccia del peso.

</dd> <dt>

<span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**\_TRACKPOSITION D3DXEVENT**
</dt> <dd>

Rilevare la posizione.

</dd> <dt>

<span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**\_TRACKENABLE D3DXEVENT**
</dt> <dd>

Abilita flag.

</dd> <dt>

<span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**\_PRIORITYBLEND D3DXEVENT**
</dt> <dd>

Valore di Blend di priorità.

</dd> <dt>

<span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




