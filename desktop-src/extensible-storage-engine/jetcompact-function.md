---
description: 'Altre informazioni su: funzione JetCompact'
title: JetCompact (funzione)
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313106"
---
# <a name="jetcompact-function"></a>JetCompact (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetcompact-function"></a>JetCompact (funzione)

La funzione **JetCompact** crea una copia di un database esistente. La copia viene compattata in uno stato ottimale per l'utilizzo. I dati nei dati copiati verranno compressi in base alle misure scelte per gli indici in fase di creazione dell'indice. In questo modo, i dati compressi possono essere archiviati nel modo più denso possibile. In alternativa, i dati compressi possono riservare spazio per gli inserimenti di indici o di crescita successivi.

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*szDatabaseSrc*

Database di origine che verrà compattato.

*szDatabaseDest*

Nome da utilizzare per il database compresso.

*pfnStatus*

Funzione di callback che può essere chiamata periodicamente tramite l'operazione di compattazione del database per segnalare lo stato di avanzamento.

*pconvert*

Puntatore utilizzato per designare una DLL ESE alternativa che può essere utilizzata per leggere il database di origine e per fornire parametri facoltativi per un'operazione **JetCompact** che converte un database da un formato precedente a una versione successiva. Questa funzionalità è stata sospesa in Windows Server 2003.

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
<td><p>JET_bitCompactRepair</p></td>
<td><p>Utilizzato quando è noto che il database di origine è danneggiato. Consente un intero set di nuovi comportamenti destinati a recuperare il maggior quantità possibile di dati dal database di origine. <strong>JetCompact</strong> con questo set di opzioni può restituire JET_errSuccess ma non copiare tutti i dati creati nel database di origine. I dati che si trovavano in parti danneggiate del database di origine verranno ignorati.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCompactStats</p></td>
<td><p>Consente a <strong>JetCompact</strong> di eseguire il dump delle statistiche nel database di origine in un file denominato DFRGINFO.TXT. Le statistiche includono il nome di ogni tabella nel database di origine, il numero di righe in ogni tabella, le dimensioni totali in byte di tutte le righe di ogni tabella, le dimensioni totali in byte di tutte le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> che erano sufficientemente grandi da essere archiviate separate dal record, il numero di pagine foglia dell'indice cluster e il numero di pagine foglia di valore lungo. Inoltre, le statistiche di riepilogo, incluse le dimensioni del database di origine, il database di destinazione, il tempo necessario per la compattazione del database, hanno anche tutti il dump dello spazio.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>È stato fornito un puntatore <em>PConvert</em> non null, ma la versione di ESE utilizzata non supporta la funzionalità di conversione. Questa funzionalità è stata rimossa nella versione di ESE di Windows Server 2003.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>La sessione chiamante si trova all'interno di una transazione. <strong>JetCompact</strong> deve essere chiamato da una sessione all'esterno di una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il database di origine viene copiato nel database di destinazione. Lo stato del database di destinazione è ottimale. ad esempio, tutti gli indici di tabella si trovano nello spazio su disco logico adiacente. Ogni pagina di indice viene riempita fino alla quantità configurata quando gli indici sono stati creati originariamente nel database di origine. Tutte le impostazioni di dati e metadati vengono copiate con la massima fedeltà, a meno che non sia stata specificata l'opzione di correzione. Se è stata specificata l'opzione di correzione, è possibile che alcuni dati del database di origine non siano stati copiati.

In caso di errore, il database di destinazione può esistere, ma non è una copia completa del database di origine.

#### <a name="remarks"></a>Commenti

La compattazione di un database viene inoltre utilizzata per aggiornare un database da un formato di versione precedente a una versione più recente. Un parametro facoltativo è *PConvert*, che contiene una struttura in grado di contenere una descrizione di una DLL di versione precedente da utilizzare per la lettura del formato del database di origine. Questa funzionalità è stata sospesa in Windows Server 2003. Successivamente a Windows Server 2003, le nuove versioni di ESE sono sempre in grado di leggere le versioni precedenti del formato del database e pertanto questa funzionalità non è necessaria.

La densità desiderata dei dati dopo un'operazione di compattazione viene specificata quando vengono creati tabelle e indici. La densità deve essere compresa tra il 20% e il 100%. Se un database viene letto e non aggiornato principalmente, le applicazioni imposteranno la densità su 100% per ridurre il numero di operazioni di I/O durante l'elaborazione della query. Tuttavia, se i dati vengono aggiornati di frequente con operazioni che aumentano le dimensioni dei dati archiviati insieme al record, o vengono inseriti di frequente nuovi dati, l'applicazione sceglierà una densità inferiore in modo che gli aggiornamenti rileveranno più spesso le risorse necessarie disponibili. Con l'operazione di compattazione del database, il database viene disposto idealmente in base al riempimento scelto dall'applicazione.

La compattazione del database è un'operazione non in linea. Non può essere eseguita mentre il database è in uso. Di conseguenza, viene in genere eseguito come parte di un processo di compilazione per lo sviluppo di un'applicazione che fornisce un set di dati come parte di se stesso.

La compattazione del database offline tocca ogni bit di dati in un database e può essere utilizzata come mezzo per verificare la coerenza di un database. Se un database è sospetto, può essere compattato. Se non viene rilevato alcun errore dalla compattazione, sarà noto che il database è in uno stato valido per ESE.

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
<td><p>Implementato come <strong>JetCompactW</strong> (Unicode) e <strong>JetCompactA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)
