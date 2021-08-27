---
description: 'Altre informazioni su: Funzione JetDetachDatabase'
title: Funzione JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a66010b5d056301e368f7221380966adc2f31180
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470466"
---
# <a name="jetdetachdatabase-function"></a>Funzione JetDetachDatabase


_**Si applica a:** Windows | Windows Server_

## <a name="jetdetachdatabase-function"></a>Funzione JetDetachDatabase

La **funzione JetDetachDatabase** rilascia un file di database precedentemente collegato a una sessione di database.

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da scollegare. Se *szFilename* è **NULL** o una stringa vuota, tutti i database collegati a *sesid* verranno scollegati.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Il backup del database è in corso e non può essere scollegato.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Il database è stato aperto <a href="gg269299(v=exchg.10).md">da JetOpenDatabase.</a> I database devono essere chiusi prima di scollegarsi.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2).</a></p> | 
| <p>JET_errInTransaction</p> | <p>È stato effettuato un tentativo di scollegare un database durante una transazione.</p> | 



#### <a name="remarks"></a>Commenti

Se un database collegato è stato aperto (con [JetAttachDatabase),](./jetattachdatabase-function.md)deve essere chiuso con [JetCloseDatabase](./jetclosedatabase-function.md) prima di scollegarlo.

Windows solo 2000: i database che non sono stati scollegati prima della chiamata a [JetTerm](./jetterm-function.md) verranno automaticamente collegati alla chiamata successiva di [JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDetachDatabaseW</strong> (Unicode) e <strong>JetDetachDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetTerm](./jetterm-function.md)
