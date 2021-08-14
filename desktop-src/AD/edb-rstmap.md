---
title: EDB_RSTMAP (Ntdsbcli.h)
description: Usato con la funzione DsRestoreRegister per eseguire il mapping di un database di cui è stato eseguito il backup a un nuovo database.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP structure Active Directory
- PEDB_RSTMAP puntatore alla struttura Active Directory
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
ms.openlocfilehash: 1c81fe35d8d41818d279df094a57c041b8ea52212d2ce2f0cdc379628f5d5971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191692"
---
# <a name="edb_rstmap-structure"></a>Struttura \_ RSTMAP EDB

La **struttura \_ RSTMAP di EDB** viene usata con la funzione [**DsRestoreRegister**](dsrestoreregister.md) per eseguire il mapping di un database di cui è stato eseguito il backup a un nuovo database.

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

Puntatore a una stringa con terminazione Null che contiene il nome del database al momento del backup.

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che contiene il nuovo nome del database, inclusa la nuova posizione, se applicabile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **EDB \_ RSTMAPW** (Unicode) ed **EDB \_ RSTMAPA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[Strutture di backup della directory](directory-backup-structures.md)
</dt> </dl>

 

 





