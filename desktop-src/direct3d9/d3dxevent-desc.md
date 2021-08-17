---
description: Descrive un evento di animazione.
ms.assetid: ddcdd143-bcbd-450c-a4df-914797a562e6
title: D3DXEVENT_DESC struttura (D3dx9anim.h)
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
ms.openlocfilehash: d5569eccd5b99939cd50797ee73593ce5a2bfc8ddd60236e05218ddcca7f4383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731809"
---
# <a name="d3dxevent_desc-structure"></a>Struttura DESC D3DXEVENT \_

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

Tipo: **[ **D3DXEVENT \_ TYPE**](./d3dxevent-type.md)**

</dd> <dd>

Tipo di evento, come definito in [**D3DXEVENT \_ TYPE**](./d3dxevent-type.md).

</dd> <dt>

**Track**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificatore della traccia dell'evento.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Ora di inizio dell'evento nell'ora globale.

</dd> <dt>

**Duration**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Durata dell'evento nel tempo globale.

</dd> <dt>

**Transizione**
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

</dd> <dd>

Stile di transizione dell'evento, come definito in [**D3DXTRANSITION \_ TYPE.**](./d3dxtransition-type.md)

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tenere traccia del peso dell'evento.

</dd> <dt>

**Velocità**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tenere traccia della velocità per l'evento.

</dd> <dt>

**Position**
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

</dd> <dd>

Tenere traccia della posizione dell'evento.

</dd> <dt>

**Abilita**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Abilita flag.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
