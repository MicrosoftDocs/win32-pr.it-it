---
description: 'Altre informazioni su: Funzione JetCompact'
title: Funzione JetCompact
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
ms.openlocfilehash: 14e79ceda56658bf8b214fff923c2df17fe8f786
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480467"
---
# <a name="jetcompact-function"></a>Funzione JetCompact


_**Si applica a:** Windows | Windows Server_

## <a name="jetcompact-function"></a>Funzione JetCompact

La **funzione JetCompact** crea una copia di un database esistente. La copia viene compattata in uno stato ottimale per l'utilizzo. I dati nei dati copiati verranno imballati in base alle misure scelte per gli indici al momento della creazione dell'indice. In questo modo, i dati compattati possono essere archiviati nel modo più denso possibile. In alternativa, i dati compattati possono riservare spazio per gli inserimenti successivi dell'indice o l'aumento delle dimensioni dei record.

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

Nome da utilizzare per il database compattato.

*pfnStatus*

Funzione di callback che può essere chiamata periodicamente tramite l'operazione di compattazione del database per segnalare lo stato di avanzamento.

*pconvert*

Puntatore utilizzato per designare una DLL ESE alternativa che può essere utilizzata per leggere il database di origine e per fornire parametri facoltativi per un'operazione **JetCompact** che converte un database da un formato precedente a un formato di versione successiva. Questa funzionalità è stata sospesa in Windows Server 2003.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitCompactRepair</p> | <p>Utilizzato quando è noto che il database di origine è danneggiato. Consente un intero set di nuovi comportamenti destinati a recuperare la maggior quantità possibile di dati dal database di origine. <strong>JetCompact</strong> con questo set di opzioni può restituire JET_errSuccess ma non copiare tutti i dati creati nel database di origine. I dati presenti in parti danneggiate del database di origine verranno ignorati.</p> | 
| <p>JET_bitCompactStats</p> | <p>Consente <strong>a JetCompact di</strong> eseguire il dump delle statistiche nel database di origine in un file denominato DFRGINFO.TXT. Le statistiche includono il nome di ogni tabella nel database di origine, il numero di righe in ogni tabella, le dimensioni totali in byte di tutte le righe in ogni tabella, le dimensioni totali in byte di tutte le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> sufficientemente grandi da essere archiviate separatamente dal record, il numero di pagine foglia dell'indice cluster e il numero di pagine foglia con valori lunghi. Vengono inoltre scaricate anche le statistiche di riepilogo, tra cui le dimensioni del database di origine, il database di destinazione, il tempo necessario per la compattazione del database e lo spazio temporaneo del database.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>È stato fornito un <em>puntatore pconvert</em> non NULL, ma la versione di ESE in uso non supporta la funzionalità di conversione. Questa funzionalità è stata rimossa nella Windows Server 2003 di ESE.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInTransaction</p> | <p>La sessione chiamante si trova all'interno di una transazione. <strong>JetCompact deve</strong> essere chiamato da una sessione all'esterno di qualsiasi transazione.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, il database di origine viene copiato nel database di destinazione. Il database di destinazione si trova in uno stato ottimale, ad esempio tutti gli indici di tabella si trovano nello spazio su disco logico adiacente. Ogni pagina di indice viene riempita fino alla quantità configurata al momento della creazione degli indici nel database di origine. Tutte le impostazioni dei dati e dei metadati vengono copiate con la massima fedeltà, a meno che non sia stata specificata l'opzione di ripristino. Se è stata specificata l'opzione di correzione, è possibile che alcuni dati del database di origine non siano stati copiati.

In caso di errore, il database di destinazione può esistere ma non è una copia completa del database di origine.

#### <a name="remarks"></a>Commenti

La compattazione di un database viene usata anche per aggiornare un database da un formato di versione precedente a una versione più moderna. Un parametro facoltativo è *pconvert*, che contiene una struttura che può contenere una descrizione per una DLL di versione precedente da usare per la lettura del formato del database di origine. Questa funzionalità è stata sospesa in Windows Server 2003. Dopo Windows Server 2003, le nuove versioni di ESE sono sempre in grado di leggere le versioni precedenti del formato del database e pertanto questa funzionalità non è necessaria.

La densità desiderata dei dati dopo un'operazione di compattazione viene specificata durante la creazione di tabelle e indici. La densità deve essere compresa tra 20% e 100%. Se un database viene principalmente letto e non aggiornato, le applicazioni impostano la densità su 100% per ridurre il numero di operazioni di I/O durante l'elaborazione delle query. Tuttavia, se i dati vengono aggiornati di frequente con operazioni che aumentano le dimensioni dei dati archiviati insieme al record o vengono spesso inseriti nuovi dati, l'applicazione sceglierà una densità inferiore in modo che gli aggiornamenti trovino più spesso le risorse necessarie disponibili. L'operazione di compattazione del database fa sì che il database sia idealmente disposto in base al riempimento scelto dall'applicazione.

La compattazione del database è un'operazione non in linea. Non può essere eseguita mentre il database è in uso. Di conseguenza, viene in genere eseguita come parte di un processo di compilazione di sviluppo di un'applicazione che fornisce un set di dati come parte di se stessa.

La compattazione del database offline tocca ogni bit di dati in un database e può essere usata per verificare la coerenza di un database. Se un database è sospetto, può essere compattato. Se non viene rilevato alcun errore durante la compattazione, sarà noto che il database è in uno stato valido per ESE.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCompactW</strong> (Unicode) e <strong>JetCompactA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)
