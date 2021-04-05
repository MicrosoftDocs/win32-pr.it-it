---
description: 'Altre informazioni su: colonne con valore Long'
title: Colonne con valore Long
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bb5618227d49de9e246adf69868a3cb2dc498dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049392"
---
# <a name="long-value-columns"></a>Colonne con valore Long


_**Si applica a:** Windows | Windows Server_

## <a name="long-value-columns"></a>Colonne con valore Long

I tipi di colonna ESE JET_coltypLongText e JET_coltypLongBinary sono denominati tipi di colonna con valore Long. Queste colonne sono stringhe di grandi dimensioni e oggetti binari di grandi dimensioni che possono essere archiviati in strutture B + separate dall'indice primario. Quando i valori Long vengono archiviati separatamente dal record primario, vengono codificati internamente su un ID di valore Long (LID) e un offset di byte e sono accessibili come flusso. Le colonne con valori di tipo Long vengono aggiunte alla tabella nella chiamata a [JetAddColumn](./jetaddcolumn-function.md) con il membro **coltyp** della struttura [JET_COLUMNDEF](./jet-columndef-structure.md) impostata su JET_coltypLongText o JET_coltypLongBinary. La dimensione massima di un testo lungo o di un valore di colonna binario lungo è 2 GB-1.

ESE supporta le operazioni di Accodamento, sovrascrittura intervallo byte e dimensioni set per le colonne con valori di tipo Long per supportare implementazioni di flusso efficienti su questi tipi di colonne. Per impostazione predefinita, i dati di valore Long vengono archiviati in un albero B + separato se è più grande di 1024 byte o se il record non rientra in una singola pagina di database quando i dati di valore lungo vengono archiviati nel record. L'applicazione ha la possibilità di eseguire l'override del comportamento predefinito impostando le opzioni per archiviare i dati di valore lungo nel record (JET_bitSetIntrinsicLV) o per forzarne l'archiviazione nell'albero B + separato (JET_bitSetIntrinsicLV). Questi valori vengono impostati nel parametro *grbit* in [JetSetColumn](./jetsetcolumn-function.md)oppure il membro **grbit** [JET_SETCOLUMN](./jet-setcolumn-structure.md) usato nella chiamata a [JetSetColumns](./jetsetcolumns-function.md) come segue:

  - Accodamento: (JET_bitSetAppendLV)

  - Sovrascrittura intervallo byte: (JET_bitSetOverwriteLV)

  - Dimensioni set: (JET_bitSetSizeLV)

  - Forza separato: (JET_bitSetSeparateLV)

  - Archivia nel record: (JET_bitSetIntrinsicLV)

I dati di valore Long vengono impostati indicando l'offset nel BLOB del valore Long e la lunghezza dei dati del valore Long nel BLOB. L'offset al BLOB del valore Long viene impostato nel membro **ibLongValue** della struttura [JET_SETINFO](./jet-setinfo-structure.md) (per [JetSetColumn](./jetsetcolumn-function.md)) o del membro **ibLongValue** della struttura [JET_SETCOLUMN](./jet-setcolumn-structure.md) (per [JetSetColumns](./jetsetcolumns-function.md)). Il membro **pvData** di [JET_SETCOLUMN](./jet-setcolumn-structure.md)e il parametro *pvData* nella chiamata a [JetSetColumn](./jetsetcolumn-function.md) contiene i dati del valore Long. Gli aggiornamenti per le colonne con valori Long devono essere eseguiti all'interno di una transazione.

I dati con valori di tipo Long vengono sempre archiviati in una tabella separata quando l'applicazione imposta il JET_bitSetSeparateLV o JET_bitSetIntrinsicLV, in caso contrario viene decisa in modo euristico. ESE archivia il valore Long separato se è più grande di 1024 byte o se il record non è adatto a una singola pagina di database se archiviato nel record.

Il diagramma seguente mostra i dati del valore Long archiviati in una tabella separata. Quando un valore Long viene archiviato all'esterno del record, viene creato un nuovo ID con valore Long per fare riferimento al relativo valore. Ciò consente a più record di fare riferimento allo stesso valore di colonna. I conteggi dei riferimenti ai dati vengono aumentati se più di un record nei dati punta agli stessi dati di valore lungo.

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

ESE supporta inoltre una singola funzionalità dell'archivio di istanze che consente a più record di fare riferimento allo stesso oggetto binario di grandi dimensioni come se ogni record avesse una propria copia delle informazioni; evitando così copie duplicate dei dati del valore della colonna. Questa funzionalità è abilitata nella chiamata a [JetPrepareUpdate](./jetprepareupdate-function.md) con l'opzione JET_prepInsertCopy impostata nel parametro *Prep* .
