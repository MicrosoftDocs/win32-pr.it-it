---
description: 'Altre informazioni su: Funzione JetSeek'
title: Funzione JetSeek
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fbc980a838742971d2ecc3dfeebf5efb6295ea3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985544"
---
# <a name="jetseek-function"></a>Funzione JetSeek


_**Si applica a:** Windows | Windows Server_

## <a name="jetseek-function"></a>Funzione JetSeek

La **funzione JetSeek** posiziona in modo efficiente un cursore in una voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e alla disuguaglianza specificata. Una chiave di ricerca deve essere stata costruita in precedenza [usando JetMakeKey.](./jetmakekey-function.md)

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata. *Grbit* deve essere diverso da zero e deve includere uno o più dei valori elencati nella tabella seguente.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitCheckUniqueness</p> | <p>Verrà restituito un codice di errore speciale, JET_wrnUniqueKey, se è possibile determinare economicamente che esiste esattamente una voce di indice che corrisponde alla chiave di ricerca.</p><p>Questa opzione viene ignorata a meno JET_bitSeekEQ non venga specificata anche l'opzione .</p><p>Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p> | 
| <p>JET_bitSeekEQ</p> | <p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che corrisponde esattamente alla chiave di ricerca. L'inizio dell'indice è la voce di indice trovata durante lo spostamento al primo record in tale indice. L'inizio dell'indice non corrisponde all'estremità più bassa dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly.</p> | 
| <p>JET_bitSeekGE</p> | <p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice maggiore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca. L'inizio dell'indice è la voce di indice trovata durante lo spostamento al primo record in tale indice. L'inizio dell'indice non corrisponde all'estremità più bassa dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly progettata per trovare le voci di indice più vicine alla fine dell'indice.</p> | 
| <p>JET_bitSeekGT</p> | <p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice maggiore di una voce di indice che corrisponde esattamente ai criteri di ricerca. L'inizio dell'indice è la voce di indice trovata durante lo spostamento al primo record in tale indice. L'inizio dell'indice non corrisponde all'estremità più bassa dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly progettata per trovare le voci di indice più vicine all'inizio dell'indice.</p> | 
| <p>JET_bitSeekLE</p> | <p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice minore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca. La fine dell'indice è la voce di indice trovata durante lo spostamento all'ultimo record dell'indice. La fine dell'indice non corrisponde all'estremità superiore dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly progettata per trovare le voci di indice più vicine all'inizio dell'indice.</p> | 
| <p>JET_bitSeekLT</p> | <p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice minore di una voce di indice che corrisponde esattamente ai criteri di ricerca. La fine dell'indice è la voce di indice trovata durante lo spostamento all'ultimo record dell'indice. La fine dell'indice non corrisponde all'estremità superiore dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly progettata per trovare le voci di indice più vicine alla fine dell'indice.</p> | 
| <p>JET_bitSetIndexRange</p> | <p>Un intervallo di indici verrà automaticamente specificato per tutte le chiavi che corrispondono esattamente alla chiave di ricerca. L'intervallo di indici risultante è identico a uno che sarebbe stato altrimenti creato da una chiamata a <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> con le opzioni JET_bitRangeInclusive e JET_bitRangeUpperLimit seguenti. Per <a href="gg294112(v=exchg.10).md">altre informazioni, vedere JetSetIndexRange.</a></p><p>Si tratta di un metodo pratico per l'individuazione di tutte le voci di indice che soddisfano gli stessi criteri di ricerca.</p><p>Questa opzione viene ignorata a meno JET_bitSeekEQ non venga specificata anche l'opzione .</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione consente la restituzione di [qualsiasi JET_ERRs](./jet-err.md) definiti in questa API. Per altre informazioni sugli errori Jet, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p><p>Per <strong>JetSeek,</strong>ciò significa che è stata trovata una voce di indice che corrisponde esattamente ai criteri di ricerca.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Non è presente alcuna chiave di ricerca corrente per il cursore. <strong>JetSeek richiede</strong> che il cursore abbia una chiave di ricerca valida perché verrà utilizzata per i criteri di ricerca utilizzati per trovare le voci di indice.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRecordNotFound</p> | <p>Non è stata trovata alcuna voce di indice corrispondente ai criteri di ricerca.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_wrnSeekNotEqual</p> | <p>È stata trovata una voce di indice corrispondente ai criteri di ricerca. Tuttavia, la voce di indice non è una corrispondenza esatta.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_wrnUniqueKey</p> | <p>È stata trovata esattamente una voce di indice che corrisponde esattamente ai criteri di ricerca. Questo errore verrà restituito solo se JET_bitSeekCheckUniqueness è stato specificato ed è stato conveniente determinare che la voce di indice corrispondente è l'unica voce di indice che corrisponde esattamente ai criteri di ricerca.</p><p>Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p> | 



In caso di esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice che corrisponde ai criteri di ricerca. Se un record è stato preparato per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo di indici verrà annullato. Se è stata costruita una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database. Quando più voci di indice hanno lo stesso valore, la voce più vicina all'inizio dell'indice viene sempre selezionata.

In caso di errore, la posizione del cursore rimarrà invariata, a meno JET_errRecordNotFound non sia stato restituito . In tal caso, il cursore verrà posizionato in corrispondenza della voce di indice corrispondente ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e in cui sarebbe stata specificata la disuguaglianza. Il cursore può essere spostato in relazione a tale posizione, ma non si trova ancora in una voce di indice valida. Se un record è stato preparato per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici, tale intervallo di indici verrà annullato. Se è stata costruita una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
