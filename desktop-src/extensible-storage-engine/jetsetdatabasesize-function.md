---
description: Altre informazioni sulla funzione JetSetDatabaseSize
title: Funzione JetSetDatabaseSize
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27799dbdbc21af4421713828633199d1c1a18973
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466228"
---
# <a name="jetsetdatabasesize-function"></a>Funzione JetSetDatabaseSize


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetdatabasesize-function"></a>Funzione JetSetDatabaseSize

La **funzione JetSetDatabaseSize** imposta le dimensioni di un file di database non aperto.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Identifica il contesto della sessione di database da usare per la chiamata API.

*szDatabaseName*

Identifica il nome del file di database di cui devono essere modificate le dimensioni.

*Cpg*

Specifica le dimensioni desiderate del database, in pagine.

*pcpgReal*

Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API. Se la chiamata API ha avuto esito negativo, il contenuto di *pcpgReal* non è definito.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>JET_errDatabaseInconsistent e JET_errDatabaseDirtyShutdown sono lo stesso valore numerico. Il database le cui dimensioni devono essere regolate deve essere in un arresto pulito, noto come stato coerente. Un database incoerente non è danneggiato, ma richiede la riproduzione dei file di log.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>szDatabaseName</em> non deve essere una stringa vuota non NULL.</p> | 
| <p>JET_errDiskFull</p> | <p>Spazio disponibile insufficiente nel volume per eseguire l'operazione di crescita. <strong>JetSetDatabaseSize</strong> può anche restituire molti errori correlati ai file, tra cui, ma non solo:</p><ul><li><p>JET_errDiskIO</p></li><li><p>JET_errFileNotFound</p></li><li><p>JET_errInvalidPath</p></li><li><p>JET_errFileAccessDenied</p></li><li><p>JET_errOutOfFileHandles</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei motivi per cui questo errore può essere restituito è se <em>cpg</em> soddisfa le dimensioni minime del database. Le dimensioni minime correnti del database sono 256 pagine.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Le risorse di memoria del sistema sono scarse.</p> | 



#### <a name="remarks"></a>Commenti

Se **jetSetDatabaseSize viene** chiamato prima di inserire grandi quantità di dati, il file di database verrà aumentato in un'unica operazione. In questo modo si ridurrà la probabilità che il file di database diventi frammentato file system livello e si ridurrà anche il numero di volte in cui il file di database deve essere aumentato. L'aumento delle dimensioni del file di database una sola volta può essere più rapido rispetto all'aumento più volte.

Attualmente è supportata solo l'espansione del file. Per compattare un file, usare la funzionalità di deframmentazione del programma esentutl.exe utilità.

Se *cpg è* inferiore alle dimensioni correnti del database, l'operazione verrà ignorata. Se *cpg è* minore delle dimensioni minime del database (attualmente 256 pagine), restituirà JET_errInvalidParameter.

Per impostare le dimensioni di un database aperto, vedere [JetGrowDatabase](./jetgrowdatabase-function.md).

Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite in *pcpgReal*. Esistono due pagine riservate aggiuntive che non possono essere conteggiate in *pcpgReal*.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetSetDatabaseSizeW</strong> (Unicode) e <strong>JetSetDatabaseSizeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
