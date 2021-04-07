---
title: Struttura EDB_RSTMAP (ntdsbcli. h)
description: Utilizzato con la funzione DsRestoreRegister per eseguire il mapping di un database di cui è stato eseguito il backup in un nuovo database.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- Struttura EDB_RSTMAP Active Directory
- Puntatore alla struttura PEDB_RSTMAP Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048481"
---
# <a name="edb_rstmap-structure"></a>\_Struttura RSTMAP edb

La **struttura \_ RSTMAP di edb** viene utilizzata con la funzione [**DsRestoreRegister**](dsrestoreregister.md) per eseguire il mapping di un database di cui è stato eseguito il backup in un nuovo database.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>Members

<dl> <dt>

**szDatabaseName**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del database in cui è stato eseguito il backup.

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nuovo nome del database, inclusa la nuova posizione, quando applicabile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **EDB \_ RSTMAPW** (Unicode) e **EDB \_ RSTMAPA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[Strutture di backup della directory](directory-backup-structures.md)
</dt> </dl>

 

 





