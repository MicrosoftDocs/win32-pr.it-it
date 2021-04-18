---
description: 'Altre informazioni su: funzione JetCreateDatabase2'
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
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316455"
---
# <a name="jetcreatedatabase2-function"></a>Funzione JetCreateDatabase2


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreatedatabase2-function"></a>Funzione JetCreateDatabase2

La funzione **JetCreateDatabase2** crea e associa un file di database da utilizzare con il motore di database ESE con le dimensioni massime del database specificate. La chiamata di **JetCreateDatabase2** con *cpgDatabaseSizeMax* impostato su zero è identica alla chiamata a [JETCREATEDATABASE](./jetcreatedatabase-function.md) con *szConnect* impostato su null. Attualmente è possibile creare fino a sette database per ogni istanza.

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

Dimensione massima delle pagine del database per il database. Le dimensioni predefinite della pagina del database sono di 4 kilobyte e possono essere modificate con [JetSetSystemParameter](./jetsetsystemparameter-function.md) prima della creazione di un database.

Il passaggio di zero indica che non viene applicato alcun valore massimo dal motore di database.

*pdbid*

Puntatore a un buffer che, in una chiamata con esito positivo, contiene l'identificatore del database. In caso di errore, il valore non è definito.

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
<td><p>Per impostazione predefinita, se viene chiamato <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> o <strong>JetCreateDatabase2</strong> e il database esiste già, la chiamata API avrà esito negativo e il database originale non verrà sovrascritto. JET_bitDbOverwriteExisting modifica questo comportamento e il database precedente verrà sovrascritto con uno nuovo. Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff disattiva la registrazione. L'impostazione di questo bit perde la possibilità di riprodurre i file di log e di ripristinare il database in uno stato utilizzabile coerente dopo un evento irreversibile.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>Impostando JET_bitDbShadowingOff si disabilita la duplicazione di alcune strutture di database interne (ombreggiatura). La duplicazione di queste strutture viene eseguita per la resilienza, quindi l'impostazione JET_bitDbShadowingOff rimuoverà tale resilienza.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

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
<td><p>Il database specificato in <em>szFileName</em> esiste già. Quando viene restituito questo errore, il database non viene collegato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Può essere restituito se è stato richiesto l'accesso esclusivo, ma non è stato possibile concederlo o se un'altra sessione ha già aperto il database in modo esclusivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Restituito quando <em>cpgDatabaseSizeMax</em> è maggiore del numero massimo di pagine consentite in un database. Il valore massimo corrente è 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>È stato specificato un percorso non valido in <em>szFileName</em>. <em>szFileName</em> deve essere non null. Per impostazione predefinita, <em>szFileName</em> deve puntare a una directory esistente. Il percorso verrà creato se <em>JET_paramCreatePathIfNotExist</em> è impostato (vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p></td>
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
<td><p>Il file di database è già stato allegato da un'altra sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>È stato effettuato un tentativo di creazione di un database in una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>È stato effettuato un tentativo di aprire un file che non è un file di database valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>È stato effettuato un tentativo di aprire più di un database e JET_paramOneDatabasePerSession è stato impostato. Vedere <a href="gg294139(v=exchg.10).md">parametri di sistema</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Le risorse del sistema sono esaurite.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Per ogni istanza è possibile collegare solo un numero finito di database. Il limite è attualmente di sette database per ogni istanza.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Avviso non irreversibile che indica che il file di database è già stato allegato da questa sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly indica che il file è stato associato in sola lettura, ma <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> non ha superato JET_bitDbReadOnly. Il database viene ancora aperto con accesso in sola lettura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Se il database specificato in *szFileName* esiste e JET_bitDbOverwriteExisting non è stato passato, la chiamata API avrà esito negativo. Se JET_bitDbOverwriteExisting è stato passato, il file di database precedente verrà eliminato per primo.

Se l'API crea un file di database e quindi raggiunge un altro errore, il file verrà eliminato ed eliminato.

Il database viene aperto in modo implicito da **JetCreateDatabase2** . Non è necessario chiamare in seguito [JetOpenDatabase](./jetopendatabase-function.md).

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
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetCreateDatabase2W</strong> (Unicode) e <strong>JetCreateDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
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
