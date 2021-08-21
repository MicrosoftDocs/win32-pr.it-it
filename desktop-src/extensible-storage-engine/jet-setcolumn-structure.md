---
description: 'Altre informazioni su: JET_SETCOLUMN Structure'
title: JET_SETCOLUMN struttura
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffdcd2ea11fad6c9ec2baae1a37bdd1965acb852
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466368"
---
# <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN struttura

La **JET_SETCOLUMN** contiene parametri di input e output per [JetSetColumns.](./jetsetcolumns-function.md) I campi nella struttura descrivono il valore della colonna da impostare, come impostarlo e dove ottenere i dati del set di colonne.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>Membri

**columnid**

Identificatore di colonna per una colonna da impostare.

**pvData**

Puntatore ai dati da impostare in una colonna.

**cbData**

Dimensione in byte dell'allocazione, a partire da **pvData.**

**grbit**

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitSetAppendLV</p> | <p>Aggiunge dati a una colonna di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> <a href="gg269213(v=exchg.10).md">o JET_coltypLongBinary</a>. Lo stesso comportamento può essere ottenuto determinando le dimensioni del valore long esistente e specificando <strong>ibLongValue</strong> in <strong>psetinfo</strong>. Tuttavia, è più semplice usare questo <em>grbit,</em>poiché non è necessario conoscere le dimensioni del valore di colonna esistente.</p> | 
| <p>JET_bitSetOverwriteLV</p> | <p>Sostituisce il valore long esistente con i nuovi dati. Quando si usa questa opzione, è come se il valore long esistente fosse stato impostato su una lunghezza pari a 0 (zero) prima di impostare i nuovi dati.</p> | 
| <p>JET_bitSetSizeLV</p> | <p>Interpreta il buffer di input come numero intero di byte da impostare come lunghezza del valore long descritto dal valore columnid specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence. Se le dimensioni specificate sono maggiori del valore della colonna esistente, la colonna verrà estesa con 0. Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</p> | 
| <p>JET_bitSetZeroLength</p> | <p>Imposta un valore su lunghezza zero. In genere, un valore di colonna viene impostato su NULL passando un valore cbMax pari a 0. Tuttavia, per alcuni tipi, ad esempio <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valore di colonna può essere di lunghezza 0 anziché NULL e questa opzione viene usata per distinguere tra la lunghezza NULL e la lunghezza 0.</p> | 
| <p>JET_bitSetSeparateLV</p> | <p>Forza l'archiviazione separata di un valore long, colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> <a href="gg269213(v=exchg.10).md">o JET_coltypLongBinary</a>, rispetto al resto dei dati del record. Ciò si verifica normalmente quando le dimensioni del valore long ne impediscono l'archiviazione con i dati dei record rimanenti. Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore long. Si noti che i valori long con dimensioni di quattro byte o inferiori non possono essere forzati per essere separati. In questi casi, l'opzione viene ignorata.</p> | 
| <p>JET_bitSetUniqueMultiValues</p> | <p>Applica valori distinti in una colonna multivalore. Questa opzione confronta i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV non possono essere fornite.</p> | 
| <p>JET_bitSetUniqueNormalizedMultiValues</p> | <p>Applica valori distinti in una colonna multivalore. Questa opzione confronta la trasformazione normalizzata della chiave dei dati della colonna con altri valori di colonna esistenti trasformati in modo simile e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV non possono essere fornite.</p> | 
| <p>JET_bitSetRevertToDefaultValue</p> | <p>Fa in modo che la colonna restituirà il valore predefinito della colonna nelle successive operazioni di recupero della colonna. Tutti i valori di colonna esistenti vengono rimossi. Questa opzione è applicabile solo alle colonne con tag, sparse o multivalore.</p> | 
| <p>JET_bitSetIntrinsicLV</p> | <p>Mantiene il valore long, le colonne di <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o JET_coltypeLongBinary, archiviate con i dati del record rimanenti, se possibile. In genere, le colonne lunghe vengono archiviate separatamente quando la lunghezza supera i 1024 byte o altrimenti la lunghezza del record supererebbe la limitazione delle dimensioni della pagina correlata. Tuttavia, se questa opzione è impostata, l'operazione di impostazione della colonna avrà esito negativo JET_errColumnTooBig anziché archiviare il valore della colonna separata dai dati del record rimanenti.</p> | 



**ibLongValue**

Offset al primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Descrive il numero di sequenza del valore in una colonna multivalore. Un **valore itagSequence** pari a 0 indica che il set di valori di colonna deve essere aggiunto come nuova istanza di una colonna multivalore.

**Err**

Codici di errore e avvisi restituiti dall'operazione set column.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)
