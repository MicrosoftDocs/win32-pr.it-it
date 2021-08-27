---
description: 'Altre informazioni su: Funzione JetCreateDatabase2'
title: Funzione JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b362b7ada2c0cc2924ce178adda2368faef770bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479207"
---
# <a name="jetcreatedatabase2-function"></a>Funzione JetCreateDatabase2


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreatedatabase2-function"></a>Funzione JetCreateDatabase2

La **funzione JetCreateDatabase2** crea e collega un file di database da usare con il motore di database ESE con le dimensioni massime specificate. La **chiamata di JetCreateDatabase2** con *cpgDatabaseSizeMax* impostata su zero è identica alla chiamata di [JetCreateDatabase](./jetcreatedatabase-function.md) con *szConnect* impostato su NULL. Attualmente è possibile creare fino a sette database per ogni istanza.

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da creare.

*cpgDatabaseSizeMax*

Dimensioni massime, in pagine di database, per il database. Le dimensioni predefinite della pagina del database sono di 4 kilobyte e possono essere modificate con [JetSetSystemParameter](./jetsetsystemparameter-function.md) prima di creare un database.

Se si passa zero, il motore di database non applica alcun valore massimo.

*pdbid*

Puntatore a un buffer che, in caso di chiamata riuscita, contiene l'identificatore del database. In caso di errore, il valore non è definito.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>Per impostazione predefinita, se viene chiamato <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> o <strong>JetCreateDatabase2</strong> e il database esiste già, la chiamata API avrà esito negativo e il database originale non verrà sovrascritto. JET_bitDbOverwriteExisting questo comportamento e il database precedente verrà sovrascritto con uno nuovo. Windows XP e versioni successive.</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff disattiva la registrazione. L'impostazione di questo bit non consente di riprodurre i file di log e ripristinare il database a uno stato utilizzabile coerente dopo un evento irreversibile.</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>L JET_bitDbShadowingOff disabilita la duplicazione di alcune strutture di database interne (shadowing). La duplicazione di queste strutture viene eseguita per la resilienza, quindi l'impostazione JET_bitDbShadowingOff rimuoverà tale resilienza.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p>Il database denominato in <em>szFilename</em> esiste già. Quando viene restituito questo errore, il database non viene collegato.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Può essere restituito se è stato richiesto l'accesso esclusivo, ma non è stato possibile concedere o se un'altra sessione ha già aperto il database in modo esclusivo.</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>Restituito <em>quando cpgDatabaseSizeMax</em> è maggiore del numero massimo di pagine consentite in un database. Il valore massimo corrente è 2147483646 (0x7ffffffe).</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>È stato specificato un percorso non valido in <em>szFilename</em>. <em>szFilename</em> deve essere diverso da NULL. Per impostazione predefinita, <em>szFilename</em> deve puntare a una directory esistente. Il percorso verrà creato se <em>JET_paramCreatePathIfNotExist</em> è impostato (vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter).</a></p> | 
| <p>JET_errDatabaseLocked</p> | <p>Indica che un'altra sessione ha già aperto il database in modo esclusivo (usando JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase).</a></p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Il file di database è già stato collegato da una sessione diversa.</p> | 
| <p>JET_errInTransaction</p> | <p>Si è tentato di creare un database in una transazione.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Si è tentato di aprire un file che non è un file di database valido.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Si è tentato di aprire più di un database ed è stato JET_paramOneDatabasePerSession stato impostato. Vedere <a href="gg294139(v=exchg.10).md">Parametri di sistema.</a></p> | 
| <p>JET_errOutOfMemory</p> | <p>Il sistema ha esaurito le risorse.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>È possibile collegare un solo numero finito di database per ogni istanza. Il limite è attualmente di sette database per istanza.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Avviso non irreversibile che indica che il file di database è già stato collegato da questa sessione.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly indica che il file è stato collegato in sola lettura, ma <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> non ha passato JET_bitDbReadOnly. Il database è ancora aperto con accesso in sola lettura.</p> | 



#### <a name="remarks"></a>Commenti

Se il database specificato in *szFilename* esiste e JET_bitDbOverwriteExisting non è stato passato, la chiamata API avrà esito negativo. Se JET_bitDbOverwriteExisting stato passato, il file di database precedente verrà eliminato per primo.

Se l'API crea un file di database e quindi genera un altro errore, pulisce ed elimina il file.

**JetCreateDatabase2 aprirà** in modo implicito il database. Non è necessario chiamare successivamente [JetOpenDatabase](./jetopendatabase-function.md).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCreateDatabase2W</strong> (Unicode) e <strong>JetCreateDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[Extensible Archiviazione Engine Files](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
