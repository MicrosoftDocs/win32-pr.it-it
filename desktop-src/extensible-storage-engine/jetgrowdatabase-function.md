---
description: Altre informazioni sulla funzione JetGrowDatabase
title: Funzione JetGrowDatabase
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 710e41b29c55ec435db6eb1b9e1536740819478e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479067"
---
# <a name="jetgrowdatabase-function"></a>Funzione JetGrowDatabase


_**Si applica a:** Windows | Windows Server_

## <a name="jetgrowdatabase-function"></a>Funzione JetGrowDatabase

La **funzione JetGrowDatabase** estende le dimensioni di un database attualmente aperto.

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*Dbid*

Database che verrà esteso.

*Cpg*

Dimensioni desiderate del database, in pagine.

*pcpgReal*

Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API. Se la chiamata API ha esito negativo, il contenuto di *pcpgReal* non è definito.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errDiskFull</p> | <p>Spazio disponibile insufficiente nel volume per eseguire l'operazione di crescita.</p> | 
| <p>JET_errDiskIO</p> | <p>Un errore correlato al file è stato restituito <a href="gg269242(v=exchg.10).md">da JetSetDatabaseSize.</a> Per altre informazioni su altri errori correlati ai file che potrebbero essere restituiti, vedere <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Commenti

Se **jetGrowDatabase viene** chiamato prima di inserire grandi quantità di dati, il file di database verrà aumentato in un'unica operazione. In questo modo si ridurrà la probabilità che il file di database diventi frammentato file system livello e si ridurrà anche il numero di volte in cui il file di database deve essere aumentato. L'aumento delle dimensioni del file di database una sola volta può essere più rapido rispetto all'aumento più volte.

Attualmente è supportata solo l'espansione del file. Per compattare un file, usare la funzionalità di deframmentazione del **programmaesentutl.exe** utilità.

Per impostare le dimensioni di un database non aperto, vedere [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite in *pcpgReal*. Esistono due pagine riservate aggiuntive che potrebbero non essere conteggiate in *pcpgReal*.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
