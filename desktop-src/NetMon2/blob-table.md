---
description: Contiene una matrice di BLOB.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Struttura BLOB_TABLE (Netmon. h)
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
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227387"
---
# <a name="blob_table-structure"></a>\_Struttura della tabella BLOB

La struttura della **\_ tabella BLOB** contiene una matrice di BLOB.

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

Indica che molti BLOB seguono.

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
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




