---
description: 'Altre informazioni su: Funzione JetSetIndexRange'
title: Funzione JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 330adc9b4d18a7bfa66ced0c9cb5776f31162be5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988454"
---
# <a name="jetsetindexrange-function"></a>Funzione JetSetIndexRange


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetindexrange-function"></a>Funzione JetSetIndexRange

La funzione **JetSetIndexRange** limita temporaneamente il set di voci di indice che il cursore può spostare usando [JetMove](./jetmove-function.md) a quelle che iniziano dalla voce di indice corrente e terminano in corrispondenza della voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e ai criteri associati specificati. Una chiave di ricerca deve essere stata costruita in precedenza [usando JetMakeKey.](./jetmakekey-function.md)

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableidSrc*

Cursore da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più degli elementi seguenti:


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitRangeInclusive</p> | <p>Questa presenza o assenza di questa opzione indica i criteri limite dell'intervallo di indici. Se presente, questa opzione indica che il limite dell'intervallo di indici è inclusivo. Se assente, questa opzione indica che il limite dell'intervallo di indici è esclusivo. Quando il limite dell'intervallo di indici è inclusivo, tutte le voci di indice che corrispondono esattamente ai criteri di ricerca vengono incluse nell'intervallo.</p> | 
| <p>JET_bitRangeInstantDuration</p> | <p>Questa opzione richiede che l'intervallo di indici venga rimosso non appena è stato stabilito. Tutti gli altri aspetti dell'operazione rimangono invariati. Ciò è utile per verificare l'esistenza di voci di indice che corrispondono ai criteri di ricerca.</p> | 
| <p>JET_bitRangeRemove</p> | <p>Questa opzione richiede l'annullamento di un intervallo di indici esistente sul cursore. Dopo l'annullamento dell'intervallo di indici, sarà possibile spostarsi oltre la fine dell'intervallo di indici usando <a href="gg294117(v=exchg.10).md">JetMove.</a> Se un intervallo di indici non è già attivo, <strong>JetSetIndexRange</strong> avrà esito negativo con JET_errInvalidOperation.</p><p>Quando questa opzione viene specificata, tutte le altre opzioni vengono ignorate.</p> | 
| <p>JET_bitRangeUpperLimit</p> | <p>Se si usa questa opzione, la chiave di ricerca nel cursore rappresenta i criteri di ricerca per la voce di indice più vicina alla fine dell'indice che corrisponderà all'intervallo di indici. L'intervallo di indici verrà stabilito tra la posizione corrente del cursore e questa voce di indice in modo che tutte le corrispondenze possano essere trovate avanzando sull'indice usando <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MoveNext o un offset positivo.</p><p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly progettata per trovare le voci di indice più vicine all'inizio dell'indice.</p><p>Se questa opzione viene omessa, la chiave di ricerca nel cursore rappresenta i criteri di ricerca per la voce di indice più vicina all'inizio dell'indice che corrisponderà all'intervallo di indici. L'intervallo di indici verrà stabilito tra la posizione corrente del cursore e questa voce di indice in modo che tutte le corrispondenze possano essere trovate tornando indietro sull'indice usando <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MovePrevious o un offset negativo.</p><p>Non è significativo omettere questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly progettata per trovare le voci di indice più vicine alla fine dell'indice.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p><p>Per <strong>JetSetIndexRange</strong>, ciò significa che un intervallo di indici esistente è stato annullato o che è presente almeno una voce di indice all'interno dell'intervallo di indici.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Questo errore verrà restituito da <strong>JetSetIndexRange</strong> quando JET_bitRangeRemove stato specificato e non era attivo alcun intervallo di indici.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Non è presente alcuna chiave di ricerca corrente per il cursore. <strong>JetSetIndexRange richiede</strong> che il cursore abbia una chiave di ricerca valida perché verrà usata per i criteri di ricerca usati per trovare le voci di indice.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Non esiste alcun indice corrente per il cursore. Questa operazione si verifica per <strong>JetSetIndexRange</strong> se il cursore si trova sull'indice cluster di una tabella e non è stato definito un indice primario. L'impostazione di un intervallo di indici su tale indice non è supportata.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Questo errore verrà restituito da <strong>JetSetIndexRange</strong> per indicare che non sono presenti voci di indice all'interno dell'intervallo di indici.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, JET_bitRangeRemove viene specificato , l'intervallo di indici attualmente attivo viene annullato. Se JET_bitRangeRemove viene o meno specificato JET_bitRangeInstantDuration, non è attivo alcun intervallo di indici. Se non JET_bitRangeRemove o JET_bitRangeInstantDuration specificato, è attivo un nuovo intervallo di indici. Questo intervallo di indici limiterà temporaneamente il set di voci di indice che il cursore può spostare utilizzando [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e terminando in corrispondenza della voce di indice che corrisponde ai criteri di ricerca. La posizione del cursore rimarrà invariata. Se è stata costruita una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, JET_errNoCurrentRecord non viene restituito alcun intervallo di indici. Se JET_errNoCurrentRecord viene restituito , è attivo un nuovo intervallo di indici. Questo intervallo di indici limiterà temporaneamente il set di voci di indice che il cursore può spostare utilizzando [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e terminando in corrispondenza della voce di indice che corrisponde ai criteri di ricerca. La posizione del cursore rimarrà invariata. Se JET_errNoCurrentRecord restituito ed è stata costruita una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Un intervallo di indici è volatile e verrà automaticamente annullato se viene eseguita una navigazione diversa [da JetMove](./jetmove-function.md) sul cursore.

Gli intervalli di indici funzionano solo in una direzione. Se viene stabilito un limite superiore, verrà impedito solo il movimento in avanti tramite [JetMove](./jetmove-function.md) con JET_MoveNext o un offset positivo una volta raggiunta la fine dell'intervallo di indici. È comunque possibile lasciare l'intervallo di indici in questo caso usando [JetMove](./jetmove-function.md) con JET_MovePrevious o un offset negativo. Si verifica una situazione analoga per un limite inferiore.

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
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
