---
description: Altre informazioni sulla funzione JetAttachDatabase2
title: Funzione JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 069339aefbac335bf1c7bb4b35efe4466b526225
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475937"
---
# <a name="jetattachdatabase2-function"></a>Funzione JetAttachDatabase2


_**Si applica a:** Windows | Windows Server_

## <a name="jetattachdatabase2-function"></a>Funzione JetAttachDatabase2

La **funzione JetAttachDatabase2** collega un file di database da usare con un'istanza del database e specifica una dimensione massima per il database. Per usare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database che verrà usato per la chiamata API.

*szFilename*

Nome del database da collegare.

*CpgDatabaseSizeMax*

Dimensioni massime, in pagine di database, per il database. Le dimensioni predefinite della pagina del database sono di 4 kilobyte, che possono essere modificate usando la funzione [JetSetSystemParameter](./jetsetsystemparameter-function.md) prima di creare un database.

Il passaggio di zero indica che il motore di database non applica il massimo.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più dei seguenti:


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> è stato impostato, tutti gli indici sui dati Unicode verranno eliminati. Per altre informazioni, vedere le sezione Osservazioni.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Tutti gli indici sui dati Unicode verranno eliminati, indipendentemente dall'impostazione <a href="gg269337(v=exchg.10).md">di JET_paramEnableIndexChecking</a>. Per altre informazioni, vedere le sezione Osservazioni.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impedisce modifiche al database.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Riservato per utilizzi futuri.</p> | 



### <a name="return-value"></a>Valore restituito

La funzione restituisce uno dei [codici](./jet-err.md) JET_ERR di errore. Di seguito sono riportati i valori restituiti più comunemente. Per un elenco completo degli errori per questa API, vedere Codici di errore del motore Archiviazione [extensible.](./extensible-storage-engine-error-codes.md)


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Il collegamento di un database non è consentito durante un backup.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Il file di database specificato <em>da szFilename</em> deve essere scrivibile. LRead-Only'attributo non deve essere impostato e il processo in esecuzione deve avere privilegi sufficienti per scrivere nel file.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Il file di database è già aperto da un altro processo.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>È stato specificato un percorso non valido in <em>szFilename</em>. <em>szFilename</em> deve essere diverso da NULL e fare riferimento a un percorso valido.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Il file di database è già stato collegato da una sessione diversa.</p> | 
| <p>JET_errFileNotFound</p> | <p>Il file specificato in <em>szFilename</em> non esiste.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Si è verificato un errore con l'indice primario. Può trattarsi di un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database per l'ultima modifica in un sistema operativo precedente e l'indice primario si trova su una colonna con dati Unicode. Per altre informazioni sugli indici sui dati Unicode, vedere le osservazioni.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Si è verificato un errore con un indice secondario. Può trattarsi di un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database per l'ultima modifica in un sistema operativo precedente e un indice secondario si trova su una colonna con dati Unicode. Per altre informazioni sugli indici sui dati Unicode, vedere le osservazioni. Gli indici secondari vengono completamente ricompilati quando un database viene deframmentato con un'utilità offline usando il comando <strong>seguente: esentutl -d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>È possibile collegare solo un numero finito di database per ogni istanza. Il limite è attualmente di sette database per istanza.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Avviso non irreversibile che indica che il file di database è già stato collegato da questa sessione.</p> | 



#### <a name="remarks"></a>Commenti

Il file di database viene scollegato [usando JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Per [le osservazioni, vedere JetAttachDatabase.](./jetattachdatabase-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetAttachDatabase2W</strong> (Unicode) e <strong>JetAttachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[File del motore Archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
