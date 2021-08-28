---
description: Altre informazioni sulla funzione JetOSSnapshotFreeze
title: Funzione JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 854e38f91b894b1f7cc486a15afcfe857aaa31d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473967"
---
# <a name="jetossnapshotfreeze-function"></a>Funzione JetOSSnapshotFreeze


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>Funzione JetOSSnapshotFreeze

La **funzione JetOSSnapshotFreeze** avvia uno snapshot. Mentre lo snapshot è in corso, non è possibile eseguire alcuna attività di scrittura su disco da parte del motore.

**Windows XP:****JetOSSnapshotFreeze** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*pcInstanceInfo*

Numero di istanze attualmente in esecuzione nel motore che fanno parte della sessione snapshot.

*paInstanceInfo*

Matrice di strutture, una per ogni istanza in esecuzione che fa parte della sessione snapshot, che descrive l'istanza e i database che ne fanno parte.

*grbit*

Opzioni per questa chiamata. Questo parametro è riservato per un uso futuro e l'unico valore valido supportato è 0.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>I puntatori forniti per i parametri di output sono NULL, la sessione snapshot non è valida o il <em>parametro grbit</em> non è valido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>La sessione snapshot non è nello stato appropriato per avviare un blocco(ad esempio, un blocco precedente non è riuscito in questa sessione in precedenza).</p> | 
| <p>JET_errOSSnapshotNotAllowed</p> | <p>Il motore non è in uno stato in cui è possibile eseguire uno snapshot. Uno o più backup di streaming sono già in corso oppure una o più istanze stanno passando i passaggi di ripristino o terminando.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L'identificatore per la sessione snapshot non è valido.</p> | 
| <p>JET_errOutOfMemory</p> | <p>La funzione non è riuscita a causa di una condizione di memoria insufficiente.</p> | 
| <p>JET_errOutOfThreads</p> | <p>La funzione non è riuscita perché non è stato possibile avviare un nuovo thread che esegue il blocco.</p> | 



Se questa funzione ha esito positivo, non verranno emesse operazioni di I/O di scrittura per i file di database o per i file di log che fanno parte di istanze bloccate. Inoltre, le informazioni sull'istanza verranno riempite correttamente e devono essere liberate in un secondo momento chiamando [JetFreeBuffer](./jetfreebuffer-function.md) con il puntatore alla matrice di informazioni sull'istanza restituita.

Se questa funzione ha esito negativo, il motore continuerà a funzionare normalmente con gli I/O che si verificano normalmente. Non è necessario chiamare [JetOSSnapshotThaw se](./jetossnapshotthaw-function.md) il blocco ha esito negativo. Inoltre, le informazioni sull'istanza non verranno compilate, quindi non è necessario liberare questa risorsa.

#### <a name="remarks"></a>Commenti

Durante il periodo di blocco, non verranno emesse operazioni di I/O di scrittura nei database collegati o nei log delle transazioni, anche se potrebbero essere presenti operazioni di I/O di scrittura rilasciate ai database temporanei o ai file di streaming.

Lo stato in cui i database e i file di log saranno durante il blocco (lo stato in cui i file si sarebbero in un'immagine snapshot del volume) sarà tale che sarà possibile un ripristino normale se tali file vengono ripristinati in un secondo momento.

Poiché non sono presenti operazioni di scrittura durante il periodo di blocco, le normali chiamate API nel motore potrebbero essere bloccate per tale intervallo. L'applicazione client deve essere in grado di gestire le chiamate API che potrebbero richiedere più tempo del normale in caso di blocco.

A causa dei possibili effetti descritti in precedenza, si verifica un timeout interno dopo il quale la sessione snapshot arresterà la fase di blocco anche se le API che eserciteranno il disgelo o l'interruzione non sono state chiamate. Il valore del timeout può essere modificato usando il parametro [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) di sistema. Si noti che l'intervallo di blocco tipico è compreso nell'intervallo di 10 secondi con il timeout predefinito di circa 60 secondi.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetOSSnapshotFreezeW</strong> (Unicode) e <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
