---
description: Altre informazioni sulla funzione JetSetCurrentIndex
title: Funzione JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 333f447805a970c111d3884caae1c016803081f2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984334"
---
# <a name="jetsetcurrentindex-function"></a>Funzione JetSetCurrentIndex


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcurrentindex-function"></a>Funzione JetSetCurrentIndex

La **funzione JetSetCurrentIndex** può essere usata per impostare l'indice corrente di un cursore. L'indice corrente di un cursore definisce i record di una tabella visibili al cursore e l'ordine in cui vengono visualizzati selezionando il set di voci di indice da usare per esporre tali record.

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*szIndexName*

Nome dell'indice da selezionare per il cursore.

Se questo parametro è NULL o una stringa vuota, verrà selezionato l'indice cluster. Se per la tabella è definito un indice primario, tale indice verrà selezionato perché corrisponde all'indice cluster. Se per la tabella non è definito alcun indice primario, verrà selezionato l'indice sequenziale. L'indice sequenziale non ha una definizione di indice. Per [altre informazioni, vedere JetCreateIndex.](./jetcreateindex-function.md)

Se *pindexid non* è NULL, il nome dell'indice verrà ignorato e l'indice verrà selezionato in base all'ID indice.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Viene selezionato un indice secondario con l'opzione JET_bitNoMove e non è presente alcun valore per la prima colonna chiave multivalore nella definizione del nuovo indice corrispondente al numero di sequenza specificato.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInvalidIndexId</p> | <p>Il contenuto dell'ID indice non è valido o è scaduto e deve essere aggiornato. Ciò può verificarsi per <strong>JetSetCurrentIndex</strong> quando:</p><ul><li><p>pindexid- &gt; cbStruct non ha le dimensioni previste (Windows Server 2003 e versioni successive).</p></li><li><p>Il motore è stato arrestato dopo il recupero dell'ID indice.</p></li><li><p>Tutti i cursori che fanno riferimento alla tabella contenente l'indice corrispondente all'ID indice sono stati chiusi e il motore ha rimosso la definizione dell'indice dalla cache dello schema.</p></li><li><p>L'ID indice viene usato con un cursore aperto nella tabella errata.</p></li><li><p>L'indice è stato eliminato o non è ancora visibile alla sessione.</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidName</p> | <p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi degli oggetti devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p><ul><li><p>I nomi degli oggetti devono essere costituiti da caratteri ASCII.</p></li><li><p>I nomi degli oggetti devono avere almeno un carattere di lunghezza.</p></li><li><p>I nomi degli oggetti non possono superare JET_cbNameMost (64) caratteri.</p></li><li><p>I nomi degli oggetti non possono iniziare con uno spazio.</p></li><li><p>I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li><li><p>I nomi degli oggetti non possono contenere un punto esclamativo (!), un punto (.), una parentesi quadra aperta ([) o una parentesi quadra chiusa (]).</p></li><li><p>Dopo la convalida, per il nome dell'oggetto verrà usata solo la parte della stringa fino al primo spazio (se presente). Ciò significa che anche i nomi degli oggetti non possono contenere uno spazio.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <strong>JetSetCurrentIndex</strong> quando <em>pindexid</em> non è NULL e pindexid- cbStruct non ha le dimensioni previste (Windows XP e versioni &gt; precedenti).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Viene selezionato un indice secondario con l'opzione JET_bitNoMove e nel nuovo indice non è presente alcuna voce di indice corrispondente al record associato alla voce di indice nella posizione corrente del cursore sull'indice precedente.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Il motore ha esaurito il pool di risorse usate per aprire i cursori. Il numero massimo di cursori che possono essere aperti in qualsiasi momento viene controllato <a href="gg269201(v=exchg.10).md">usando</a>JET_paramMaxCursors . Per <a href="gg294044(v=exchg.10).md">altre informazioni, vedere JetSetSystemParameter.</a> Ciò può verificarsi per <strong>JetSetCurrentIndex</strong> quando è stato selezionato un indice secondario e il motore non può aprire un cursore interno per usare tale indice.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, l'indice corrente del cursore viene impostato sull'indice richiesto. È ora possibile cercare le voci di indice [usando JetSeek](./jetseek-function.md) in base alla definizione dell'indice richiesto. Le voci di indice possono anche essere enumerate usando [JetMove](./jetmove-function.md) nell'ordine specificato dalla definizione dell'indice. La posizione corrente del cursore è impostata sulla prima voce di indice nell'indice (JET_bitMoveFirst) o su una voce di indice specifica correlata alla posizione corrente del cursore sull'indice precedente (JET_bitNoMove). Non verrà apportata alcuna modifica allo stato del database.

In caso di errore, l'indice corrente e la posizione corrente del cursore sono in uno stato non definito. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se l'hint per l'ID indice non è valido, l'API ha semplicemente esito negativo. In questo caso non è previsto alcun fallback al nome di testo dell'indice. Questo fallback deve essere eseguito manualmente dal chiamante dell'API.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetSetCurrentIndexW</strong> (Unicode) e <strong>JetSetCurrentIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetCurrentIndex]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
