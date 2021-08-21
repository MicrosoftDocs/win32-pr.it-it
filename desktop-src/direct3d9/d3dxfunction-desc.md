---
description: Descrive una funzione usata da un effetto.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: D3DXFUNCTION_DESC struttura (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: fb67f99daa1c0ed551ce989c15e9be2d1f89f8352dfebf7a021ea16f7c69f49e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525658"
---
# <a name="d3dxfunction_desc-structure"></a>Struttura DESC D3DXFUNCTION \_

Descrive una funzione usata da un effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome funzione.

</dd> <dt>

**Annotazioni**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Non utilizzato. Questo membro verrà sempre impostato su zero da [**GetFunctionDesc.**](id3dxbaseeffect--getfunctiondesc.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
