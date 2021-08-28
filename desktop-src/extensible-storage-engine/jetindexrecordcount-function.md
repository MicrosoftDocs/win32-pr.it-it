---
description: 'Altre informazioni su: Funzione JetIndexRecordCount'
title: Funzione JetIndexRecordCount
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4105dec0217c1fea2e00d92c9d217fcf2d7e40b4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480437"
---
# <a name="jetindexrecordcount-function"></a>Funzione JetIndexRecordCount


_**Si applica a:** Windows | Windows Server_

## <a name="jetindexrecordcount-function"></a>Funzione JetIndexRecordCount

La **funzione JetIndexRecordCount** conta il numero di voci nell'indice corrente dalla posizione corrente in avanti. La posizione corrente è inclusa nel conteggio. Il conteggio può essere maggiore del numero totale di record nella tabella se l'indice corrente si trova su una colonna multivalore e le istanze della colonna hanno più valori. Se la tabella è vuota, per il conteggio verrà restituito 0.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*pcrec*

Puntatore a un valore long senza segno per ricevere il conteggio.

*crecMax*

Numero massimo di record da contare. Un *valore crecMax* pari a 0 indica che il conteggio è illimitato.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>L'operazione non può essere completata perché tutte le attività nell'istanza associata alla sessione sono scadute in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>L'operazione non può essere completata perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non si trova attualmente in un record e la tabella non è vuota.</p><p><strong>Windows XP, Windows Server 2003, Windows 2000 Server e Windows 2000 Professional:</strong>  Se il cursore è posizionato in corrispondenza di un indice vuoto o di un intervallo di indici, <strong>JetIndexRecordCount</strong> restituisce erroneamente JET_errNoCurrentRecord.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, il numero esatto di voci di indice, inclusa la posizione corrente e fino a *crecMax* (se non è 0), viene restituito nell'oggetto unsigned long a cui punta *pcrec*.

Se questa funzione ha esito negativo, non vengono apportate modifiche alla memoria allocata *in corrispondenza di precpos*.

#### <a name="remarks"></a>Commenti

Se la tabella non è vuota, il cursore deve essere posizionato sul record da cui iniziare il conteggio. Il conteggio includerà questo record e verrà conteggiato in avanti fino al limite specificato in *crecMax*. Se *crecMax è* 0, l'operazione continuerà a contare fino alla fine dell'indice.

Gli intervalli di indici possono essere usati per costruire limitazioni artificiali di fine indice per il conteggio. In questo modo, gli intervallo secondari di un indice possono essere conteggiati esattamente. Il cursore deve essere posizionato sulla prima riga dell'intervallo. È necessario impostare la fine della chiave dell'intervallo e quindi [usare JetSetIndexRange](./jetsetindexrange-function.md) per impostare l'intervallo superiore, in modo inclusivo o esclusivo. Infine, **è necessario chiamare JetIndexRecordCount** per contare esattamente l'intervallo.

**JetIndexRecordCount** rispetta la semantica delle transazioni e restituisce un conteggio accurato per questa sessione specifica nello stato transazionale corrente.

**JetIndexRecordCount accede** alle pagine foglia dell'indice per contare esattamente le voci. Di conseguenza, può eseguire una grande quantità di operazioni di I/O e può essere lento. La *limitazione crecMax* deve essere usata per evitare un carico eccessivo. Se un intervallo è grande, potrebbe essere possibile contare l'intervallo in modo approssimativo usando [JetGetRecordPosition.](./jetgetrecordposition-function.md)

**Windows XP, Windows Server 2003, Windows 2000 Server e Windows 2000 Professional:**  Se il cursore è posizionato in corrispondenza di un indice vuoto o di un intervallo di indici, **JetIndexRecordCount** restituisce erroneamente JET_errNoCurrentRecord anziché restituire un numero di record pari a zero. In questo caso, l'applicazione deve verificare se l'indice o l'intervallo di indici è vuoto.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
