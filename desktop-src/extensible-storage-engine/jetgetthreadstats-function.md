---
description: 'Altre informazioni su: funzione JetGetThreadStats'
title: JetGetThreadStats (funzione)
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305737"
---
# <a name="jetgetthreadstats-function"></a>JetGetThreadStats (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetthreadstats-function"></a>JetGetThreadStats (funzione)

La funzione **JetGetThreadStats** recupera le informazioni sulle prestazioni dal motore di database per il thread corrente. È possibile utilizzare più chiamate per raccogliere statistiche che riflettono l'attività del motore di database in questo thread tra le chiamate.

**Windows Vista:**  **JetGetThreadStats** è stato introdotto in Windows Vista.

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parametri

*pvResult*

Buffer di output che riceve i dati delle statistiche del thread. Il buffer contiene una struttura di [JET_THREADSTATS](./jet-threadstats-structure.md) dopo una chiamata eseguita correttamente.

*cbMax*

Dimensione massima in byte del buffer di output.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>L'operazione non è riuscita perché il buffer di output specificato è troppo piccolo per contenere i dati richiesti. La funzione <strong>JetGetThreadStats</strong> restituirà questo errore quando il buffer di output è troppo piccolo per contenere la versione più piccola della struttura <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> supportata dal motore di database.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il buffer di output conterrà una struttura [JET_THREADSTATS](./jet-threadstats-structure.md) contenente le statistiche del motore di database per il thread corrente.

In caso di errore, lo stato del buffer di output non è definito.

#### <a name="remarks"></a>Commenti

Le informazioni fornite da due chiamate consecutive di questa API sono destinate a essere usate per calcolare i costi di qualsiasi altra operazione del motore di database nel thread corrente. In genere, questa operazione viene eseguita eseguendo prima e dopo la lettura delle statistiche e sottraendo il conteggio after dal conteggio before per ottenere il conteggio netto delle operazioni eseguite.

Ad esempio, un'applicazione può chiamare **JetGetThreadStats** una volta per ottenere una lettura iniziale delle statistiche per il thread corrente. Potrebbe quindi chiamare la funzione [JetMove](./jetmove-function.md) con il parametro *cRow* impostato su JET_MoveNext per passare alla voce di indice successiva in un indice. Potrebbe quindi chiamare di nuovo **JetGetThreadStats** per ottenere un'altra lettura delle statistiche del thread. Potrebbe quindi sottrarre il contatore cPageReferenced dalla seconda lettura dalla prima. Il risultato è il numero di pagine di database a cui il motore di database fa riferimento per eseguire l'operazione [JetMove](./jetmove-function.md) .

Le statistiche per ogni thread vengono accumulate per la durata di tale thread. Le statistiche vengono reimpostate se la DLL del motore di database viene scaricata dal processo host.

La struttura di [JET_THREADSTATS](./jet-threadstats-structure.md) verrà probabilmente espansa in futuro per contenere più statistiche. Le nuove statistiche verranno aggiunte alla fine della struttura e potranno essere recuperate con una dimensione del buffer di output maggiore. La presenza di statistiche aggiuntive può essere dedotta da un valore cbStruct più grande.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)
