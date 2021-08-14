---
description: Statistiche sulle risorse raccolte dal ResourceManager D3DDEVINFO \_ quando si usa il meccanismo di query asincrono.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Struttura D3DRESOURCESTATS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc992c5b8246ce302cda8924b8521c923575c8914c83b35c8c1e789e4bc1c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527473"
---
# <a name="d3dresourcestats-structure"></a>Struttura D3DRESOURCESTATS

Statistiche sulle risorse raccolte dal [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) quando si usa il meccanismo di query asincrono.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**bThrashing**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Indica se è in corso la thrashing.

</dd> <dt>

**ApproxBytesDownloaded**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero approssimativo di byte scaricati da Resource Manager.

</dd> <dt>

**NumEvicts**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di oggetti che sono stati sgomberati.

</dd> <dt>

**NumVidCreates**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di oggetti creati nella memoria video.

</dd> <dt>

**LastPri**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Priorità dell'ultimo oggetto che è stato sgomberato.

</dd> <dt>

**NumUsed**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di oggetti impostati sul dispositivo.

</dd> <dt>

**NumUsedInVidMem**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di oggetti impostati sul dispositivo, che sono già presenti nella memoria video.

</dd> <dt>

**WorkingSet**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di oggetti nella memoria video.

</dd> <dt>

**WorkingSetBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di byte nella memoria video.

</dd> <dt>

**TotalManaged**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero totale di oggetti gestiti.

</dd> <dt>

**TotalBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero totale di byte di oggetti gestiti.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Notifica asincrona (Direct3D 9)](asynchronous-notification.md)
</dt> </dl>

 

 
