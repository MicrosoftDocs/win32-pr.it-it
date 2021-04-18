---
description: Descrive un evento di animazione.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: Struttura D3DXEVENT_DESC (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 32e02e75d3d73569b60c466f45dace2c074a6b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322706"
---
# <a name="d3dxevent_desc-structure"></a>\_Struttura D3DXEVENT DESC

Descrive un evento di animazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXEVENT_DESC {
  D3DXEVENT_TYPE      Type;
  UINT                Track;
  DOUBLE              StartTime;
  DOUBLE              Duration;
  D3DXTRANSITION_TYPE Transition;
  union {
    FLOAT  Weight;
    FLOAT  Speed;
    DOUBLE Position;
    BOOL   Enable;
  };
} D3DXEVENT_DESC, *LPD3DXEVENT_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXEVENT \_**](./d3dxevent-type.md)**

</dd> <dd>

Tipo di evento, come definito [**nel \_ tipo D3DXEVENT**](./d3dxevent-type.md).

</dd> <dt>

**Track**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificatore di traccia eventi.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Ora di inizio dell'evento nell'ora globale.

</dd> <dt>

**Duration**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Durata dell'evento nell'ora globale.

</dd> <dt>

**Transizione**
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**

</dd> <dd>

Stile di transizione dell'evento, come definito nel [**\_ tipo D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Tenere traccia del peso dell'evento.

</dd> <dt>

**Velocità**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Rilevare la velocità per l'evento.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

</dd> <dd>

Rilevare la posizione per l'evento.

</dd> <dt>

**Attiva**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Abilita flag.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
