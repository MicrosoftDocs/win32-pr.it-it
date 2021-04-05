---
description: 'Altre informazioni su: struttura JET_SETCOLUMN'
title: Struttura JET_SETCOLUMN
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750519"
---
# <a name="jet_setcolumn-structure"></a>Struttura JET_SETCOLUMN


_**Si applica a:** Windows | Windows Server_

## <a name="jet_setcolumn-structure"></a>Struttura JET_SETCOLUMN

La struttura **JET_SETCOLUMN** contiene i parametri di input e di output per [JetSetColumns](./jetsetcolumns-function.md). I campi della struttura descrivono il valore della colonna da impostare, come impostarlo e dove ottenere i dati del set di colonne.

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

**ColumnID**

Identificatore di colonna per una colonna da impostare.

**pvData**

Puntatore ai dati da impostare in una colonna.

**cbData**

Dimensione dell'allocazione, in byte, a partire da **pvData** in byte.

**grbit**

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Accoda i dati a una colonna di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. È possibile ottenere lo stesso comportamento determinando la dimensione del valore Long esistente e specificando <strong>ibLongValue</strong> in <strong>psetinfo</strong>. Tuttavia, è più semplice usare questo <em>grbit</em>, poiché la conoscenza delle dimensioni del valore della colonna esistente non è necessaria.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Sostituisce il valore Long esistente con i nuovi dati. Quando si utilizza questa opzione, è come se il valore Long esistente fosse stato impostato su 0 (zero) lunghezza prima dell'impostazione dei nuovi dati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Interpreta il buffer di input come numero intero di byte da impostare come lunghezza del valore Long descritto dal ColumnID specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence. Se la dimensione specificata è maggiore del valore della colonna esistente, la colonna verrà estesa con 0. Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Imposta un valore di lunghezza zero. In genere, un valore di colonna è impostato su NULL passando un cbMax di 0. Tuttavia, per alcuni tipi, ad esempio <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valore di colonna può essere di lunghezza 0 anziché null e questa opzione viene utilizzata per distinguere la lunghezza tra null e 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Forza un valore Long, le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, da archiviare separatamente dal resto dei dati del record. Questa situazione si verifica in genere quando la dimensione del valore Long impedisce che venga archiviata con i dati dei record rimanenti. Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore Long. Si noti che non è possibile forzare la separazione dei valori long di quattro byte o di dimensioni inferiori. In questi casi, l'opzione viene ignorata.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Applica valori distinct in una colonna multivalore. Questa opzione consente di confrontare i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Applica valori distinct in una colonna multivalore. Questa opzione Confronta la principale trasformazione normalizzata dei dati della colonna con altri valori di colonna in modo analogo e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLv, JET_bitSetOverwriteLV e JET_bitSetSizeLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Determina la restituzione del valore di colonna predefinito da parte della colonna nelle successive operazioni di recupero colonne. Tutti i valori di colonna esistenti vengono rimossi. Questa opzione è applicabile solo per le colonne con tag, sparse o multivalore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Mantiene il valore Long, le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o JET_coltypeLongBinary, archiviate con i dati record rimanenti, se possibile. Normalmente, le colonne lunghe vengono archiviate separatamente quando la loro lunghezza supera i 1024 byte o altrimenti la lunghezza del record supera la limitazione della dimensione relativa alle dimensioni della pagina. Tuttavia, se questa opzione è impostata, l'operazione set Column avrà esito negativo e si verificherà un errore JET_errColumnTooBig anziché archiviare questo valore di colonna separato dai dati rimanenti del record.</p></td>
</tr>
</tbody>
</table>


**ibLongValue**

Offset al primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md)o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Descrive il numero di sequenza del valore in una colonna multivalore. Il valore 0 di **itagSequence** indica che il set di valori di colonna deve essere aggiunto come nuova istanza di una colonna multivalore.

**Err**

Codici di errore e avvisi restituiti dall'operazione set Column.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)
