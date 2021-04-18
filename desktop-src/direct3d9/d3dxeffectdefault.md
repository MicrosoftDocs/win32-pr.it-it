---
description: Effetti sui parametri predefiniti.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Struttura D3DXEFFECTDEFAULT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322709"
---
# <a name="d3dxeffectdefault-structure"></a>Struttura D3DXEFFECTDEFAULT

Effetti sui parametri predefiniti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a>Members

<dl> <dt>

**pParamName**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nome del parametro.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**

</dd> <dd>

Tipo di dati in pValue. Per ulteriori informazioni, vedere [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**NumBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione, in byte, dei dati a cui punta pValue.

</dd> <dt>

**pValue**
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Puntatore alla posizione di memoria che contiene i dati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
