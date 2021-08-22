---
description: Contiene una matrice di OGGETTI BLOB.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: BLOB_TABLE struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e0615ad9c11657a47d9eaa87035207cb499634cd4ded6ae484d6f5d256c23e15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144344"
---
# <a name="blob_table-structure"></a>Struttura \_ BLOB TABLE

La **struttura \_ BLOB TABLE** contiene una matrice di OGGETTI BLOB.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNumBlobs**
</dt> <dd>

Indicatore che seguono molti BLOB.

</dd> <dt>

**hBlobs**
</dt> <dd>

Handle per la matrice BLOB.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




