---
description: 'Altre informazioni su: Colonne con valori lunghi'
title: Colonne con valori lunghi
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: deab012a7dd1496d8fc772369d63a94f8a5f47d8e9675c1e78a10ab658a4efe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703531"
---
# <a name="long-value-columns"></a>Colonne con valori lunghi


_**Si applica a:** Windows | Windows Server_

## <a name="long-value-columns"></a>Colonne con valori lunghi

I tipi di colonna ESE JET_coltypLongText e JET_coltypLongBinary sono denominati tipi di colonna con valori lunghi. Queste colonne sono stringhe di grandi dimensioni e oggetti binari di grandi dimensioni che possono essere archiviati in alberi B+ separati lontano dall'indice primario. Quando i valori long vengono archiviati separatamente dal record primario, vengono memorizzati internamente su un ID valore lungo (LID) e un offset di byte e vi si accede come flusso. Le colonne con valori lunghi vengono aggiunte alla tabella nella chiamata a [JetAddColumn](./jetaddcolumn-function.md) con il membro **coltyp** della struttura [JET_COLUMNDEF](./jet-columndef-structure.md) impostato su JET_coltypLongText o JET_coltypLongBinary. La dimensione massima di un valore di colonna Long Text o Long Binary è 2 GB -1.

ESE supporta operazioni di accodamento, sovrascrittura dell'intervallo di byte e impostazione delle dimensioni per le colonne con valori lunghi per supportare implementazioni di flussi efficienti su questi tipi di colonna. Per impostazione predefinita, i dati di valore long vengono archiviati in un albero B+ separato se sono maggiori di 1024 byte o se il record non rientra in una singola pagina del database quando i dati del valore long vengono archiviati nel record. L'applicazione può eseguire l'override del comportamento predefinito impostando le opzioni per archiviare i dati di valore lungo nel record (JET_bitSetIntrinsicLV) o per forzarne l'archiviazione nell'albero B+ separato (JET_bitSetIntrinsicLV). Questi valori vengono impostati nel *parametro grbit* in [JetSetColumn](./jetsetcolumn-function.md)o nel membro **grbit** JET_SETCOLUMN usato nella chiamata a [JetSetColumns](./jetsetcolumns-function.md) come indicato di seguito: [](./jet-setcolumn-structure.md)

  - Append: (JET_bitSetAppendLV)

  - Sovrascrittura intervallo di byte: (JET_bitSetOverwriteLV)

  - Imposta dimensioni: (JET_bitSetSizeLV)

  - Forza separazione: (JET_bitSetSeparateLV)

  - Archivia nel record: (JET_bitSetIntrinsicLV)

I dati del valore long vengono impostati indicando l'offset nel BLOB con valore long e la lunghezza dei dati del valore long nel BLOB. L'offset per il BLOB di valori long è impostato nel membro **ibLongValue** della struttura [JET_SETINFO](./jet-setinfo-structure.md) (per [JetSetColumn](./jetsetcolumn-function.md)) o nel membro **ibLongValue** della struttura [JET_SETCOLUMN](./jet-setcolumn-structure.md) (per [JetSetColumns).](./jetsetcolumns-function.md) Il **membro pvData** [JET_SETCOLUMN](./jet-setcolumn-structure.md)parametro , e *pvData* nella chiamata a [JetSetColumn](./jetsetcolumn-function.md) contiene i dati del valore long. Gli aggiornamenti alle colonne con valori lunghi devono essere eseguiti all'interno di una transazione.

I dati del valore long vengono sempre archiviati in una tabella separata quando l'applicazione imposta il JET_bitSetSeparateLV o JET_bitSetIntrinsicLV, in caso contrario viene deciso in modo euristico. ESE archivia il valore long separato se è maggiore di 1024 byte o se il record non rientra in una singola pagina di database se archiviato nel record.

Il diagramma seguente illustra i dati del valore long archiviati in una tabella separata. Quando un valore long viene archiviato all'esterno del record, viene creato un nuovo ID con valori long per fare riferimento al relativo valore. Ciò consente a più record di fare riferimento allo stesso valore di colonna. I conteggi dei riferimenti ai dati vengono aumentati se più record nei dati puntano agli stessi dati di valore lungo.

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

ESE supporta anche una funzionalità dell'archivio a istanza singola che consente a più record di fare riferimento allo stesso oggetto binario di grandi dimensioni come se ogni record avesse una propria copia delle informazioni; evitando così copie duplicate dei dati del valore della colonna. Questa funzionalità è abilitata nella chiamata a [JetPrepareUpdate](./jetprepareupdate-function.md) con l JET_prepInsertCopy opzione impostata nel *parametro prep.*
