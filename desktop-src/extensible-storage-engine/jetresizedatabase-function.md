---
description: 'Altre informazioni su: Funzione JetResizeDatabase'
title: Funzione JetResizeDatabase
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dd7faf1a28d6cafe7b33e4df49f32c631bb699e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477527"
---
# <a name="jetresizedatabase-function"></a>Funzione JetResizeDatabase


_**Si applica a:** Windows | Windows Server_

La **funzione JetResizeDatabase** estende o compatta le dimensioni di un database attualmente aperto.

La **funzione JetResizeDatabase** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*Dbid*

Database che verrà esteso.

*Cpg*

Dimensioni richieste del database, in pagine.

*pcpgActual*

Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API. Se la chiamata API non riesce, il contenuto del *parametro pcpgActual* non è definito.

*grbit*

Gruppo di bit che specifica zero o più valori elencati nella tabella seguente.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitResizeDatabaseOnlyGrow</p> | <p>Aumentare solo le dimensioni del database. Se la chiamata di ridimensionamento compatta il database, non eseguire alcuna operazione.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE [(Extensible](./extensible-storage-engine-errors.md) Archiviazione Engine), vedere Extensible Archiviazione Engine Errors and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errDiskFull</p> | <p>Lo spazio disponibile nel volume non è sufficiente per eseguire l'operazione di crescita.</p> | 
| <p>JET_errDiskIO</p> | <p>La funzione <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> ha restituito un errore correlato al file. Per altre informazioni su altri errori correlati ai file che potrebbero essere restituiti, vedere <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize.</a></p> | 



#### <a name="remarks"></a>Commenti

Se la **funzione JetResizeDatabase** viene chiamata prima di inserire grandi quantità di dati, il file di database verrà aumentato in un'unica operazione. In questo modo si riduce la probabilità che il file di database diventi frammentato a livello di file system e si riduce anche il numero di volte in cui è necessario aumentare le dimensioni del file di database. L'aumento delle dimensioni del file di database una volta può essere più veloce rispetto all'aumento delle dimensioni più volte.

Per impostare le dimensioni di un database non aperto, vedere [JetSetDatabaseSize.](./jetsetdatabasesize-function.md)

Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite nel *parametro pcpgReal.* Due pagine riservate aggiuntive potrebbero non essere conteggiate nel *parametro pcpgReal.*

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows 8.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2012.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
