---
description: 'Altre informazioni su: funzione JetOSSnapshotFreeze'
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
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232739"
---
# <a name="jetossnapshotfreeze-function"></a>Funzione JetOSSnapshotFreeze


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotfreeze-function"></a>Funzione JetOSSnapshotFreeze

La funzione **JetOSSnapshotFreeze** avvia uno snapshot. Durante l'esecuzione dello snapshot, non è possibile eseguire alcuna attività Write-to-disk da parte del motore.

**Windows XP:**  **JetOSSnapshotFreeze** è stato introdotto in Windows XP.

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

Opzioni per questa chiamata. Questo parametro è riservato per utilizzi futuri e l'unico valore valido supportato è 0.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>I puntatori forniti per i parametri di output sono NULL, la sessione snapshot non è valida o il parametro <em>grbit</em> non è valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>La sessione snapshot non è nello stato appropriato per avviare un blocco (ad esempio, un blocco precedente non è riuscito in questa sessione).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed</p></td>
<td><p>Il motore non si trova in uno stato in cui può essere eseguito uno snapshot. Uno o più backup di streaming sono già in corso o una o più istanze passano attraverso i passaggi di ripristino o terminano.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Identificatore per la sessione snapshot non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>La funzione non è riuscita a causa di una condizione di memoria insufficiente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads</p></td>
<td><p>La funzione non è riuscita perché non è stato possibile avviare un nuovo thread che esegue il blocco.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, non verranno eseguiti IOs di scrittura per i file di database o per i file di log che fanno parte di istanze bloccate. Inoltre, le informazioni sull'istanza verranno compilate correttamente e devono essere liberate in un secondo momento chiamando [JetFreeBuffer](./jetfreebuffer-function.md) con il puntatore alla matrice di informazioni sull'istanza restituita.

Se questa funzione ha esito negativo, il motore continuerà a funzionare normalmente con l'IOs che si verifica come di consueto. Non è necessario chiamare [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) se il blocco non riesce. Inoltre, le informazioni sull'istanza non verranno compilate, quindi non è necessario liberare questa risorsa.

#### <a name="remarks"></a>Commenti

Durante il periodo di blocco, non verranno rilasciati IOs di scrittura nei database collegati o nei log delle transazioni, anche se potrebbe essere stata eseguita la scrittura di IOs nei database temporanei o nei file di streaming.

Lo stato in cui si troveranno i database e i file di log durante il blocco, ovvero lo stato in cui si trovano i file in un'immagine di snapshot del volume, sarà tale da consentire un ripristino normale se tali file vengono ripristinati in un secondo momento.

Poiché non sono presenti operazioni di scrittura durante il periodo di blocco, le normali chiamate API nel motore potrebbero essere bloccate per tale intervallo. L'applicazione client deve essere in grado di gestire le chiamate API che potrebbero richiedere più tempo del normale se si verifica un blocco.

A causa dei possibili effetti descritti in precedenza, si verifica un timeout interno dopo il quale la sessione snapshot arresterà la fase di blocco anche se non sono state chiamate le API che hanno eseguito lo sblocco o l'interruzione. Il valore del timeout può essere modificato usando il [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) parametro di sistema. Si noti che l'intervallo di blocco tipico è compreso nell'intervallo di 10 secondi con il timeout predefinito in un punto intorno a 60 secondi.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetOSSnapshotFreezeW</strong> (Unicode) e <strong>JetOSSnapshotFreezeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
