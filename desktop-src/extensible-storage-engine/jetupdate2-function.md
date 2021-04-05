---
description: 'Altre informazioni su: funzione JetUpdate2'
title: Funzione JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750474"
---
# <a name="jetupdate2-function"></a>Funzione JetUpdate2


_**Si applica a:** Windows | Windows Server_

## <a name="jetupdate2-function"></a>Funzione JetUpdate2

La funzione **JetUpdate2** esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente. Questa funzione contiene un elenco di opzioni di *grbit* che possono essere impostate durante l'esecuzione di un aggiornamento. L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete](./jetdelete-function.md).

**Windows server 2003: JetUpdate2** è stato introdotto in windows Server 2003.

**JetUpdate2** è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando [JetPrepareUpdate](./jetprepareupdate-function.md) e chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o più volte per impostare lo stato del record. Infine, **JetUpdate2** viene chiamato per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo da [JetUpdate](./jetupdate-function.md) o **JetUpdate2** e non durante [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md).

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pvBookmark*

Puntatore a un segnalibro restituito per una riga inserita.

*cbBookmark*

Dimensioni del buffer a cui punta *pvBookmark*.

*pcbActual*

Dimensioni restituite del segnalibro per la riga inserita restituita in *pvBookmark*.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.

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
<td><p>JET_bitUpdateCheckESE97Compatibility</p></td>
<td><p>Questo flag fa in modo che l'aggiornamento restituisca un errore se l'aggiornamento non è stato possibile nella versione Windows 2000 di ESE, che ha applicato un numero massimo di istanze di colonna multivalore inferiore in ogni record rispetto alle versioni successive di ESE. Questo aspetto è importante solo per le applicazioni che vogliono replicare i dati tra le applicazioni ospitate in Windows 2000 e le applicazioni ospitate in Windows Server 2003 o versioni successive di ESE. Non dovrebbe essere necessario per la maggior parte delle applicazioni.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Il buffer specificato per il segnalibro di record non è sufficientemente grande per l'archiviazione del segnalibro del record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>L'operazione di aggiornamento richiede la crescita del file di database o l'allocazione dei file di log, ma l'unità disco in cui risiede il file di database o la serie di log è piena. In alternativa, il file di database si trova in un volume formattato FAT32 e il file di database è già 4GBytes, il limite per file per FAT32.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Il parametro <em>Prep</em> specificato nella funzione <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> non è un flag valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate</p></td>
<td><p>Una chiave di indice per questo record è un duplicato di un'altra chiave di indice per un altro record già presente nella tabella e l'indice non consente duplicati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated</p></td>
<td><p>Il record inserito o aggiornato presenta uno o più indici per i quali la chiave generata avrebbe superato le dimensioni massime consentite. Di conseguenza, l'operazione non è riuscita a impedire il troncamento della chiave.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation</p></td>
<td><p>Il record inserito o aggiornato ha una colonna multivalore indicizzata con due o più valori identici all'interno delle dimensioni della chiave di lunghezza massima impostate per l'indice. Di conseguenza, nel record sono presenti due voci identiche nell'indice che non sono valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Una o più colonne del record da inserire o nello stato aggiornato di un record da sostituire è <strong>null</strong> , che viola il vincolo definito per tali colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed</p></td>
<td><p>Uno o più indici sono definiti per non consentire una chiave <strong>null</strong> e lo stato inserito o aggiornato di un record sostituito viola questo vincolo definito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordPrimaryChanged</p></td>
<td><p>Un'operazione di sostituzione di record ha aggiornato la chiave primaria. Gli aggiornamenti alle colonne chiave primaria devono essere eseguiti tramite l'eliminazione del record esistente e l'inserimento di un nuovo record con i dati desiderati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> è stato chiamato con JET_prepCancel ma il cursore non si trovava nello stato preparato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflict</p></td>
<td><p>Un'operazione di sostituzione di record per cui un blocco di scrittura non è già stato allocato può riscontrare un conflitto di scrittura al momento dell'aggiornamento.</p></td>
</tr>
</tbody>
</table>


Al termine dell'operazione, l'operazione di apertura aggiornamento sul cursore viene completata. Se per la tabella è definita una colonna con incremento automatico, questo valore viene impostato per i record inseriti. Se per la tabella è definita una colonna della versione, il relativo valore viene inizializzato per i nuovi record inseriti o incrementato ogni volta che un record viene sostituito. Tutti gli indici, inclusi gli indici cluster e non cluster, vengono aggiornati.

In caso di errore, non viene apportata alcuna modifica al database. È possibile che siano state richiamate le funzioni di callback before INSERT e before, ma dopo che i callback di Replace e After non sono state richiamate, poiché quest'ultimo non può causare errori di aggiornamento. Il buffer di copia del cursore viene lasciato nello stato preparato, in modo che esista un'opportunità per correggere in modo incrementale i problemi che hanno causato errori e ripetere l'operazione di aggiornamento.

#### <a name="remarks"></a>Commenti

Le limitazioni relative alle dimensioni dei record vengono applicate da [JetSetColumn](./jetsetcolumn-function.md)e non in generale da [JetUpdate](./jetupdate-function.md). L'unica eccezione si verifica quando viene utilizzato il flag di compatibilità JET_bitUpdateCheckESE97Compatibility. In questo caso, l'intero record viene controllato perché una singola operazione [JetSetColumn](./jetsetcolumn-function.md) che supera il limite può essere compensata da una chiamata successiva a [JetSetColumn](./jetsetcolumn-function.md).

Per ulteriori informazioni, vedere la sezione Osservazioni in [JetUpdate](./jetupdate-function.md) .

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
