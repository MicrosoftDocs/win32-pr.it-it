---
description: 'Altre informazioni su: Funzione JetMove'
title: Funzione JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0d00578f4f66af0b0cef76cef7193d0174e253a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983394"
---
# <a name="jetmove-function"></a>Funzione JetMove


_**Si applica a:** Windows | Windows Server_

## <a name="jetmove-function"></a>Funzione JetMove

La **funzione JetMove** posiziona un cursore all'inizio o alla fine di un indice e attraversa le voci in tale indice in avanti o indietro. È anche possibile spostare il cursore avanti o indietro sull'indice corrente di un numero specificato di voci di indice. Un altro approccio consiste nel limitare artificialmente le voci di indice enumerabili tramite **JetMove** configurando un intervallo di indici sul cursore [usando JetSetIndexRange](./jetsetindexrange-function.md).

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*Corvo*

Offset arbitrario che indica lo spostamento desiderato del cursore sull'indice corrente.

Oltre agli offset standard, questo parametro può essere impostato anche con una delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_MoveFirst</p> | <p>Sposta il cursore sulla prima voce di indice nell'indice ( se presente).</p><p><strong>Nota:</strong>   Il valore letterale -2147483648 viene usato per indicare questa opzione. Non usare questo valore come offset normale o potrebbe verificarsi un comportamento imprevisto.</p> | 
| <p>JET_MoveLast</p> | <p>Sposta il cursore sull'ultima voce di indice nell'indice (se presente).</p><p><strong>Nota:</strong>   Il valore letterale di 2147483647 viene usato per indicare questa opzione. Non usare questo valore come offset normale o potrebbe verificarsi un comportamento imprevisto.</p> | 
| <p>JET_MoveNext</p> | <p>Sposta il cursore alla voce di indice successiva nell'indice (se presente). Questo valore è esattamente uguale a un offset normale pari a +1.</p> | 
| <p>JET_MovePrevious</p> | <p>Sposta il cursore sulla voce di indice precedente nell'indice (se presente).</p><p>Questo valore è esattamente uguale a un offset normale di -1 o 0 (zero).</p><p>Il cursore rimane nella posizione logica corrente e verrà testata l'esistenza della voce di indice corrispondente a tale posizione logica.</p> | 



*grbit*

Gruppo di bit che specificano zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitMoveKeyNE</p> | <p>Sposta il cursore avanti o indietro in base al numero di voci di indice necessarie per ignorare il numero richiesto di valori di chiave dell'indice rilevati nell'indice. Ciò ha l'effetto di compressione delle voci di indice con valori di chiave duplicati in una singola voce di indice. In genere, un offset sposta il cursore in base al numero specificato di voci di indice indipendentemente dai relativi valori di chiave.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita. Per <strong>JetMove</strong>, ciò significa che è stata trovata una voce di indice nella posizione o nell'offset richiesto nell'indice corrente.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è attualmente posizionato su una voce di indice. Per <strong>JetMove</strong>, ciò significa che non è stata trovata una voce di indice nella posizione o nell'offset richiesto nell'indice corrente.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Il cursore è attualmente posizionato logicamente su una voce di indice corrispondente a un record eliminato.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice corrispondente alla posizione o all'offset richiesto. Se è stato preparato un record per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici JET_MoveFirst o JET_MoveLast è stato specificato, tale intervallo verrà annullato. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la posizione del cursore rimarrà invariata a meno JET_errNoCurrentRecord restituito. In tal caso, il cursore verrà posizionato in corrispondenza della voce di indice corrispondente alla posizione o all'offset richiesto. Il cursore può essere spostato rispetto a tale posizione, ma non si trova ancora in una voce di indice valida. Se è stato preparato un record per l'aggiornamento, tale aggiornamento verrà annullato. Se è attivo un intervallo di indici JET_MoveFirst o JET_MoveLast è stato specificato, tale intervallo verrà annullato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Un cursore può essere spostato in due posizioni speciali usando **JetMove**, Before First e After Last. Se il cursore si trova sulla prima voce di indice nella tabella e **JetMove** viene chiamato con JET_MovePrevious, la chiamata avrà esito negativo con JET_errNoCurrentRecord e il cursore verrà posizionato logicamente prima della prima voce nell'indice. Questa posizione logica viene mantenuta anche se viene inserita un'altra voce di indice prima della prima voce nell'indice. Si verifica una situazione analoga per After Last rispetto alla fine dell'indice. Prima di First e After Last sono particolarmente utili quando si configura un intervallo di voci di indice da iterare usando **JetMove**, usando un modello di iteratore che prevede di passare sempre all'elemento successivo (o precedente) prima di usare tale elemento.

Il set di voci di indice che possono essere visitate **da JetMove** può essere limitato impostando un intervallo di indici sul cursore. Ciò è utile per le applicazioni che enumerano un set di voci di indice che corrispondono a criteri semplici che possono essere espressi tramite una coppia di chiavi di ricerca create per tale indice. Per altre informazioni, vedere [JetSetIndexRange.](./jetsetindexrange-function.md)

Nelle versioni precedenti a Windows Server 2003 SP1 si verifica un problema in **JetMove** che si verifica in alcuni casi specifici, che influisce sulla corretta applicazione di un intervallo di indici come impostato dalla [funzione JetSetIndexRange.](./jetsetindexrange-function.md) Se il cursore è attualmente prima della prima voce di indice e un intervallo di indici è impostato con un limite superiore inferiore alla prima voce di indice, la chiamata successiva a **JetMove** andrà erroneamente a tale voce di indice invece di avere esito negativo con JET_errNoCurrentRecord, come previsto. Lo stesso errore si verifica per la situazione analoga a partire dalla fine dell'indice. Questa situazione può verificarsi in un'applicazione che configura un intervallo di indici e lo esplora usando un iteratore che prevede di iniziare prima della prima voce di indice membro del set di voci da enumerare, anziché iniziare dalla prima voce di indice del set. Questa situazione si verifica anche nel caso analogo a partire dalla fine dell'indice. La soluzione alternativa consiste nel verificare manualmente che la voce di indice acquisita sia all'interno dell'intervallo di indici confrontando la chiave per la voce di indice corrente (recuperata tramite [JetRetrieveKey](./jetretrievekey-function.md)) con la chiave che rappresenta la fine dell'intervallo di indici corrente (recuperata usando [JetRetrieveKey](./jetretrievekey-function.md) usando JET_bitRetrieveCopy).

È importante prestare attenzione quando si passano offset calcolati a **JetMove**. Se l'offset calcolato è minore o uguale a JET_MoveFirst, tale offset deve essere suddiviso in più parti, ognuna delle quali viene passata a **JetMove** separatamente ma all'interno di una singola transazione per ottenere l'effetto desiderato. Lo stesso vale per gli offset maggiori o uguali a JET_MoveNext. È improbabile che un'applicazione possa essere sottoposta a questa operazione nel mondo reale, ma è utile avere una difesa da questo caso data la semantica molto diversa di JET_MoveFirst e JET_MoveLast da un offset normale.

Quando **JetMove** viene chiamato con un offset molto grande, ad esempio quando il parametro cRow è impostato su 1000, **JetMove** attraversa tutte le 1000 voci di indice per raggiungere la posizione finale. Attualmente, l'API ESE non offre un modo efficiente per passare direttamente a una determinata voce di indice in base all'offset senza attraversare ogni voce di indice.

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
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
