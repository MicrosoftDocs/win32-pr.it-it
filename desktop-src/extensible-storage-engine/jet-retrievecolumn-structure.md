---
description: 'Altre informazioni su: struttura JET_RETRIEVECOLUMN'
title: Struttura JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 688728e74d81055922f9e7e748dea1f30faa3548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308028"
---
# <a name="jet_retrievecolumn-structure"></a>Struttura JET_RETRIEVECOLUMN


_**Si applica a:** Windows | Windows Server_

## <a name="jet_retrievecolumn-structure"></a>Struttura JET_RETRIEVECOLUMN

La struttura **JET_RETRIEVECOLUMN** contiene i parametri di input e di output per [JetRetrieveColumns](./jetretrievecolumns-function.md). I campi della struttura descrivono il valore della colonna da recuperare, il modo in cui recuperarlo e il percorso in cui salvare i risultati.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Membri

**ColumnID**

Identificatore di colonna per la colonna da recuperare.

**pvData**

Puntatore per iniziare a archiviare i dati recuperati dal valore della colonna.

**cbData**

Dimensione dell'allocazione a partire da **pvData**, in byte. Tramite l'operazione di recupero colonna non vengono archiviati più dati in **pvData** rispetto a **cbData**.

**cbActual**

Dimensione, in byte, dei dati recuperati da un'operazione di recupero colonna.

**grbit**

Gruppo di bit che contiene le opzioni per il recupero di colonne, che includono zero o più dei valori seguenti.

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Recupera il valore modificato anziché il valore originale. Se il valore non è stato modificato, viene recuperato il valore originale. In questo modo, è possibile recuperare un valore che non è ancora stato inserito o aggiornato quando si inserisce o si aggiorna un record.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Recupera i valori di colonna dall'indice senza accedere al record, se possibile. In questo modo, è possibile evitare il caricamento di record superflui quando sono disponibili dati necessari dalle voci dell'indice. Nei casi in cui non è possibile recuperare il valore della colonna originale dall'indice a causa di trasformazioni irreversibili o troncamenti dei dati, il record sarà accessibile e i dati verranno recuperati normalmente. Si tratta di un'opzione relativa alle prestazioni e deve essere specificata solo quando è probabile che il valore della colonna possa essere recuperato dall'indice. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster, perché le voci di indice per l'indice cluster o primario sono i record stessi. Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromPrimaryBookmark.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Recupera i valori di colonna dal segnalibro dell'indice e può essere diverso dal valore di indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario. Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromIndex.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Recupera il numero di sequenza di un valore di colonna multivalore in pretinfo- &gt; itagSequence. Il campo itagSequence viene spesso usato come input per il recupero di valori di colonna multivalore da un record. Tuttavia, quando si recuperano i valori da un indice, è anche possibile associare la voce di indice a un determinato numero di sequenza e recuperare anche questo numero di sequenza. Il recupero del numero di sequenza può essere un'operazione costosa e deve essere eseguito solo se necessario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ bitRetrieveNull</p></td>
<td><p>Recupera i valori NULL della colonna multivalore. Se questa opzione non è specificata, i valori NULL della colonna multivalore verranno automaticamente ignorati.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Causa la restituzione di un valore NULL quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record. Questa opzione ha effetto solo sulle colonne multivalore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</p></td>
</tr>
</tbody>
</table>


**ibLongValue**

Offset al primo byte da recuperare da una colonna di tipo [JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Numero di sequenza dei valori contenuti in una colonna multivalore. **itagSequence** qui nell' **JET_RETRIEVECOLUMN** può essere 0. Se **itagSequence** è 0, viene restituito il numero di istanze di una colonna multivalore anziché dati di colonna. Non è possibile usare un valore **itagSequence** pari a 0 nelle chiamate a [JetRetrieveColumn](./jetretrievecolumn-function.md).

**columnidNextTagged**

**ColumnID** della colonna contrassegnata, multivalore o di tipo sparse quando tutte le colonne con tag vengono recuperate passando 0 come **ColumnID** a [JetRetrieveColumn](./jetretrievecolumn-function.md).

**Err**

Codici di errore e avvisi restituiti dal recupero della colonna.

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
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
