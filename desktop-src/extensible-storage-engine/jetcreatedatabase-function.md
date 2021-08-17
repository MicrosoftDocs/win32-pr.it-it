---
description: Altre informazioni sulla funzione JetCreateDatabase
title: Funzione JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 788c8e9fcc97d834843f42752d59cd6c8754fd49b99eac829ed5a68ae18cf287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358301"
---
# <a name="jetcreatedatabase-function"></a>Funzione JetCreateDatabase


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreatedatabase-function"></a>Funzione JetCreateDatabase

La **funzione JetCreateDatabase** crea e collega un file di database da usare con il motore di database ESE. Chiamare [JetCreateDatabase2](./jetcreatedatabase2-function.md) con *cpgDatabaseSizeMax* impostato su zero è identico a chiamare **JetCreateDatabase** con *szConnect* impostato su NULL. Attualmente è possibile creare fino a sette database per ogni istanza.

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da creare.

*szConnect*

Riservato per utilizzi futuri. Impostata su NULL.

*pdbid*

Puntatore a un buffer che, in caso di chiamata riuscita, contiene l'identificatore del database. In caso di errore, il valore non è definito.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDbOverwriteExisting</p></td>
<td><p>Per impostazione predefinita, se <strong>viene chiamato JetCreateDatabase</strong> e il database esiste già, la chiamata API avrà esito negativo e il database originale non verrà sovrascritto. JET_bitDbOverwriteExisting questo comportamento e il database precedente verrà sovrascritto con uno nuovo. Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff disattiva la registrazione. L'impostazione di questo bit perde la possibilità di riprodurre i file di log e ripristinare il database in uno stato utilizzabile coerente dopo un evento irreversibile.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>L JET_bitDbShadowingOff disabilita la duplicazione di alcune strutture di database interne (shadowing). La duplicazione di queste strutture viene eseguita per la resilienza, quindi l'impostazione JET_bitDbShadowingOff rimuoverà tale resilienza.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Errori del motore Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p>Il database denominato in <em>szFilename</em> esiste già. Quando viene restituito questo errore, il database non viene collegato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Può essere restituito se è stato richiesto l'accesso esclusivo, ma non è stato possibile concedere o se un'altra sessione ha già aperto il database in modo esclusivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Restituito <em>quando cpgDatabaseSizeMax è</em> maggiore del numero massimo di pagine consentite in un database. Il valore massimo corrente è 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>È stato specificato un percorso non valido in <em>szFilename</em>. <em>szFilename</em> deve essere diverso da NULL. Per impostazione predefinita, <em>szFilename</em> deve puntare a una directory esistente. Il percorso verrà creato <em>se</em> JET_paramCreatePathIfNotExist è impostato (vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Indica che un'altra sessione ha già aperto il database in modo esclusivo (usando JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Il file di database è già stato collegato da una sessione diversa.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>È stato effettuato un tentativo di creare un database durante una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>È stato effettuato un tentativo di aprire un file che non è un file di database valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>È stato effettuato un tentativo di aprire più di un database ed è JET_paramOneDatabasePerSession stato impostato. Vedere <a href="gg269337(v=exchg.10).md">Parametri di database</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>È possibile collegare solo un numero finito di database per ogni istanza. Il limite è attualmente di sette database per istanza.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Avviso non irreversibile che indica che il file di database è già stato collegato da questa sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly indica che il file è stato collegato in sola lettura, ma <strong>JetCreateDatabase</strong> non ha passato JET_bitDbReadOnly. Il database è ancora aperto con accesso in sola lettura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Se il database specificato in *szFilename* esiste e JET_bitDbOverwriteExisting non è stato passato, la chiamata API avrà esito negativo. Se JET_bitDbOverwriteExisting passato, il file di database precedente verrà eliminato per primo.

Se l'API crea un file di database e quindi viene visualizzato un altro errore, pulirà ed eliminerà il file.

**JetCreateDatabase aprirà** in modo implicito il database. Non è necessariamente necessario chiamare successivamente [JetOpenDatabase](./jetopendatabase-function.md).

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetCreateDatabaseW</strong> (Unicode) e <strong>JetCreateDatabaseA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore Archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
