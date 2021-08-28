---
description: Altre informazioni sulla funzione JetIntersectIndexes
title: Funzione JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9cb24ab9457cbad421d91764323b1db0e56a1ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468908"
---
# <a name="jetintersectindexes-function"></a>Funzione JetIntersectIndexes


_**Si applica a:** Windows | Windows Server_

## <a name="jetintersectindexes-function"></a>Funzione JetIntersectIndexes

La **funzione JetIntersectIndexes** calcola l'intersezione tra più set di voci di indice da indici secondari diversi sulla stessa tabella. Questa operazione è utile per trovare il set di record in una tabella che corrispondono a due o più criteri che possono essere espressi tramite intervalli di indici.

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*rgindexrange*

Puntatore a una matrice [di JET_IndexRange](./jet-indexrange-structure.md) struttura . Ogni struttura include [un JET_TABLEID](./jet-tableid.md) che è stato configurato per contenere uno degli intervalli di indici da intersecare. Per altre informazioni, vedere [JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

Numero di [JET_IndexRange](./jet-indexrange-structure.md) nella matrice contenuta nel *parametro rgindexrange.*

*precordlist*

Puntatore a una [JET_RECORDLIST](./jet-recordlist-structure.md) struttura . Questa struttura verrà popolata con informazioni sufficienti per attraversare la tabella temporanea con i risultati di **JetIntersectIndexes.**

Buffer di output che riceve una [JET_RECORDLIST](./jet-recordlist-structure.md) struttura . La struttura contiene una descrizione del set di risultati dell'intersezione.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sugli errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una delle opzioni richieste non è valida, usata in modo errato o non è implementata.</p><p>Questo errore viene restituito <strong>da JetIntersectIndexes</strong> quando:</p><p>Il <em>grbit</em> contenuto nella <a href="gg269335(v=exchg.10).md">struttura JET_IndexRange</a> a cui punta qualsiasi elemento nella matrice <em>rgindexrange</em> non è uguale a JET_bitRecordInIndex.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o un valore incoerente se combinato con il valore di un altro parametro.</p><p>Questo errore viene restituito <strong>da JetIntersectIndexes</strong> per i motivi seguenti:</p><ul><li><p>Il <em>parametro precordlist</em> è NULL.</p></li><li><p>Il <strong>membro cbStruct</strong> della <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> specificata nel <em>parametro precordlist</em> non è uguale alle dimensioni <a href="gg269287(v=exchg.10).md">della JET_RECORDLIST</a> struttura.</p></li><li><p>Il <em>parametro cindexrange</em> è zero.</p></li><li><p>Il <em>parametro cindexrange</em> è maggiore di 64.</p></li><li><p>Il <strong>membro cbStruct</strong> per qualsiasi elemento <a href="gg269335(v=exchg.10).md">della matrice</a> specificato dal parametro <em>rgindexrange</em> non è uguale alle dimensioni della JET_IndexRange struttura .</p></li><li><p>Gli elementi nella <em>matrice rgindexrange</em> contengono <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>da tabelle diverse.</p></li><li><p>Un elemento nella <em>matrice rgindexrange</em> contiene un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> non posizionato in corrispondenza di un indice secondario.</p></li><li><p>Uno o più elementi nella matrice <em>rgindexrange</em> contengono JET_TABLEID <a href="gg269182(v=exchg.10).md">posizionati</a>sullo stesso indice secondario.</p></li></ul> | 
| <p>JET_errInvalidSesid</p> | <p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p><p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo con il massimo sforzo.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata inizializzata.</p> | 
| <p>JET_errOutOfCursors</p> | <p>L'operazione non è riuscita perché il motore non è riuscito ad allocare le risorse necessarie per aprire un nuovo cursore. Le risorse cursore vengono <a href="gg294044(v=exchg.10).md">configurate chiamando JetSetSystemParameter</a> <em>con JET_paramMaxCursors</em> specificato nel <em>parametro paramid.</em></p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p><p><strong>JetIntersectIndexes</strong> può restituire JET_errOutOfMemory se lo spazio indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporanee alloca sempre un blocco di 1 MB di spazio di indirizzi per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare. <strong>JetIntersectIndexes</strong> creerà una tabella temporanea per ogni <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specificato nel parametro <em>rgindexrange</em> e una tabella temporanea per l'output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Non è valido usare la stessa sessione da più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>L'operazione non è riuscita perché il motore non è riuscito ad allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Il numero di indici il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxOpenTables <em>specificato</em> nel <em>parametro paramid.</em></p> | 
| <p>JET_errTooManyOpenTables</p> | <p>L'operazione non è riuscita perché il motore non è riuscito ad allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxOpenTables <em>specificato</em> nel <em>parametro paramid.</em></p> | 
| <p>JET_errTooManySorts</p> | <p>L'operazione non è riuscita perché il motore non è riuscito ad allocare le risorse necessarie per creare una tabella temporanea. Le risorse della tabella temporanea vengono <a href="gg294044(v=exchg.10).md">configurate usando JetSetSystemParameter</a> con JET_paramMaxTemporaryTables specificato nel <em>parametro paramid.</em></p> | 



In caso di esito positivo, viene restituita una nuova tabella temporanea contenente i segnalibri dei record che corrispondono ai criteri rappresentati da ogni descrizione dell'intervallo di indici di input.

In caso di errore, la tabella temporanea contenente i risultati non verrà creata. Lo stato del database temporaneo può essere modificato. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato. La posizione corrente dei [JET_TABLEID](./jet-tableid.md)forniti a questa funzione può essere modificata.

#### <a name="remarks"></a>Commenti

**È possibile usare JetIntersectIndexes** per filtrare in modo efficiente i record in una tabella in base a più criteri se tali criteri possono essere espressi in termini di indici secondari su tale tabella. Si consideri, ad esempio, una tabella molto grande contenente persone. La tabella può contenere colonne per l'ID utente, il nome, il cognome e così via. Si supponga che ognuna di queste colonne sia indicizzata separatamente e che l'indice primario della tabella sia superiore all'ID utente. Per trovare tutti gli utenti il cui nome inizia con A e il cui cognome inizia con G, seguire questa procedura:

1.  Aprire un nuovo cursore sulla tabella e impostare tale cursore in modo che utilizzi l'indice sulla colonna "first name". Configurare quindi un intervallo di indici per tutte le persone il cui "nome" inizia con ["A"](./jet-indexrange-structure.md) e compilare uno struct JET_IndexRange che contiene questo cursore.

2.  Ripetere il passaggio 1 con un nuovo cursore sull'indice "cognome" per tutte le persone il cui "cognome" inizia con "G".

3.  Passare questi criteri **a JetIntersectIndexes** per calcolare il risultato in una tabella temporanea.

4.  Attraversare la tabella temporanea e recuperare ognuno dei record che superano i criteri in base al segnalibro.

La tabella temporanea contenente il set di risultati è una tabella semplice con una colonna contenente il segnalibro di ogni record che ha superato tutti i criteri utilizzati per calcolare l'intersezione. Il set di risultati viene ordinato nello stesso ordine dell'indice primario e non contiene voci duplicate. L'applicazione può enumerare i risultati dell'intersezione enumerando le righe nella tabella temporanea, recuperando il segnalibro per ogni risultato [usando JetRetrieveColumn](./jetretrievecolumn-function.md)e quindi visitando il record nel database chiamando [JetGotoBookmark](./jetgotobookmark-function.md) con tale segnalibro su un cursore posizionato sull'indice primario.

La tabella temporanea restituita **da JetIntersectIndexes** può essere analizzata solo in avanti. Deve essere chiusa anche tramite [JetCloseTable](./jetclosetable-function.md) al termine dell'analisi. Per altre informazioni sulle tabelle temporanee e sul loro funzionamento, vedere [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

**JetIntersectIndexes è** in genere un modo efficiente e pratico per filtrare i record in base a più criteri indicizzati. Tuttavia, è necessario seguire alcuni suggerimenti importanti per ottimizzare l'utilità di questa funzionalità. Se si è a sapere che uno dei criteri è così restrittivo che l'intervallo di indici risultante ha pochi record, è probabilmente meglio semplicemente eseguire la ricerca di tale intervallo di indici e filtrare i record a livello di applicazione. Inoltre, se si sa di avere criteri molto meno restrittivi rispetto ad altri criteri nell'intersezione, è possibile eliminare tali criteri molto meno restrittivi dall'intersezione. Infine, se si sa che uno dei criteri non è affatto restrittivo, in modo che l'intervallo di indici risultante sia quasi grande come l'indice primario, è improbabile che l'intersezione con tale intervallo di indici possa trarre vantaggio (ridurre le dimensioni del) set di risultati. In tutti i casi, è consigliabile selezionare i criteri in modo da ottenere il numero minimo di voci di indice possibili nell'input e generare il set più specifico di segnalibri nell'output per ottenere prestazioni massime.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
