---
description: Altre informazioni sulla funzione JetDetachDatabase2
title: Funzione JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4f29253f3b320abb662f7a4334a14c1c49ed546
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984884"
---
# <a name="jetdetachdatabase2-function"></a>Funzione JetDetachDatabase2


_**Si applica a:** Windows | Windows Server_

## <a name="jetdetachdatabase2-function"></a>Funzione JetDetachDatabase2

La **funzione JetDetachDatabase2** rilascia un file di database precedentemente collegato a una sessione del database.

**Windows XP:****JetDetachDatabase2** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da scollegare. Se *szFilename* è **NULL** o una stringa vuota, tutti i database collegati a *sesid* verranno scollegati.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>Forza la chiusura e lo scollegamento del database. Se JET_bitForceCloseAndDetach non è supportato, JET_errForceDetachNotAllowed verrà restituito .</p> | 
| <p>JET_bitForceDetach</p> | <p>Forza lo scollegamento del database. Se JET_bitForceDetach non è supportato, JET_errForceDetachNotAllowed verrà restituito .</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>È in corso il backup del database e non è possibile scollegarlo.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Il database è stato aperto <a href="gg269299(v=exchg.10).md">da JetOpenDatabase.</a> I database devono essere chiusi prima di scollegarsi.</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2).</a></p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>JET_bitForceDetach non è supportato.</p> | 
| <p>JET_errInTransaction</p> | <p>Si è tentato di scollegare un database durante una transazione.</p> | 



#### <a name="remarks"></a>Commenti

Se un database collegato è stato aperto (con [JetAttachDatabase),](./jetattachdatabase-function.md)deve essere chiuso con [JetCloseDatabase](./jetclosedatabase-function.md) prima di scollegarsi.

Windows solo 2000: i database che non sono stati scollegati prima di chiamare [JetTerm](./jetterm-function.md) verranno automaticamente ricollegato alla successiva chiamata di [JetInit.](./jetinit-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDetachDatabase2W</strong> (Unicode) e <strong>JetDetachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetTerm](./jetterm-function.md)
