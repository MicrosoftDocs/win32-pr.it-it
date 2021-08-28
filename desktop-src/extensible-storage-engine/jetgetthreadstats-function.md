---
description: Altre informazioni sulla funzione JetGetThreadStats
title: Funzione JetGetThreadStats
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
ms.openlocfilehash: 87f3bed1dcd9fd43a67c96cbcb53d2496a976afa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474087"
---
# <a name="jetgetthreadstats-function"></a>Funzione JetGetThreadStats


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetthreadstats-function"></a>Funzione JetGetThreadStats

La **funzione JetGetThreadStats** recupera informazioni sulle prestazioni dal motore di database per il thread corrente. È possibile usare più chiamate per raccogliere statistiche che riflettono l'attività del motore di database in questo thread tra tali chiamate.

**Windows Vista:****JetGetThreadStats** è stato introdotto in Windows Vista.  

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parametri

*pvResult*

Buffer di output che riceve i dati delle statistiche del thread. Il buffer contiene una [struttura JET_THREADSTATS](./jet-threadstats-structure.md) dopo una chiamata riuscita.

*cbMax*

Dimensione massima in byte del buffer di output.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L'operazione non è riuscita perché il buffer di output specificato è troppo piccolo per contenere i dati richiesti. La <strong>funzione JetGetThreadStats</strong> restituirà questo errore quando il buffer di output è troppo piccolo per contenere la versione più piccola della struttura <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> supportata dal motore di database.</p> | 



In caso di esito positivo, il buffer di output conterrà [JET_THREADSTATS](./jet-threadstats-structure.md) che contiene le statistiche del motore di database per il thread corrente.

In caso di errore, lo stato del buffer di output non è definito.

#### <a name="remarks"></a>Commenti

Le informazioni fornite da due chiamate consecutive di questa API devono essere usate per calcolare le spese di qualsiasi altra operazione del motore di database sul thread corrente. In genere, questa operazione viene eseguita prendendo un prima e dopo la lettura delle statistiche e sottraendo il conteggio after dal conteggio before per ottenere il conteggio netto delle operazioni eseguite.

Ad esempio, un'applicazione potrebbe **chiamare JetGetThreadStats** una volta per ottenere una lettura iniziale delle statistiche per il thread corrente. Potrebbe quindi chiamare la [funzione JetMove con](./jetmove-function.md) il parametro *cRow* impostato su JET_MoveNext per passare alla voce di indice successiva in un indice. Potrebbe quindi chiamare **di nuovo JetGetThreadStats** per ottenere un'altra lettura delle statistiche del thread. Potrebbe quindi sottrarre il contatore cPageReferenced dalla seconda lettura dalla prima. Il risultato è il numero di pagine di database a cui fa riferimento il motore di database per eseguire [l'operazione JetMove.](./jetmove-function.md)

Le statistiche per ogni thread vengono accumulate per la durata di tale thread. Le statistiche vengono reimpostate se la DLL del motore di database viene scaricata dal processo host.

La [JET_THREADSTATS](./jet-threadstats-structure.md) struttura verrà probabilmente espansa in futuro per contenere altre statistiche. Le nuove statistiche verranno aggiunte alla fine della struttura e potranno essere recuperate con dimensioni del buffer di output maggiori. La presenza di statistiche aggiuntive può essere dedotto da un valore cbStruct più grande.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)
