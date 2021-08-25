---
description: 'Altre informazioni su: JET_RETRIEVECOLUMN struttura'
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
ms.openlocfilehash: 4f29f3c6a9ca3262b3cd09d726634afd70db9c6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471457"
---
# <a name="jet_retrievecolumn-structure"></a>Struttura JET_RETRIEVECOLUMN


_**Si applica a:** Windows | Windows Server_

## <a name="jet_retrievecolumn-structure"></a>Struttura JET_RETRIEVECOLUMN

La **JET_RETRIEVECOLUMN** contiene i parametri di input e output [per JetRetrieveColumns.](./jetretrievecolumns-function.md) I campi nella struttura descrivono il valore della colonna da recuperare, come recuperarlo e dove salvare i risultati.

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

**columnid**

Identificatore di colonna per la colonna da recuperare.

**pvData**

Puntatore per iniziare l'archiviazione dei dati recuperati dal valore della colonna.

**cbData**

Dimensione dell'allocazione a partire **da pvData**, in byte. L'operazione di recupero colonna non archivierà più dati in **pvData rispetto** **a cbData**.

**cbActual**

Dimensione, in byte, dei dati recuperati da un'operazione di recupero colonna.

**grbit**

Gruppo di bit che contengono le opzioni per il recupero delle colonne, che includono zero o più dei valori seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Recupera il valore modificato anziché il valore originale. Se il valore non è stato modificato, viene recuperato il valore originale. In questo modo, è possibile recuperare un valore che non è ancora stato inserito o aggiornato quando viene inserito o aggiornato un record.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Recupera i valori di colonna dall'indice senza accedere al record, se possibile. In questo modo, è possibile evitare il caricamento non necessario dei record quando i dati necessari sono disponibili dalle voci di indice stesse. Nei casi in cui non è possibile recuperare il valore della colonna originale dall'indice, a causa di trasformazioni irreversibili o troncamento dei dati, si accede al record e i dati vengono recuperati come di consueto. Si tratta di un'opzione per le prestazioni e deve essere specificata solo quando è probabile che il valore della colonna possa essere recuperato dall'indice. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster, poiché le voci di indice per l'indice cluster o primario sono i record stessi. Questo bit non può essere impostato se JET_bitRetrieveFromPrimaryBookmark è impostato.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Recupera i valori di colonna dal segnalibro dell'indice e può differire dal valore dell'indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario. Questo bit non può essere impostato se JET_bitRetrieveFromIndex è impostato.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Recupera il numero di sequenza di un valore di colonna multivalore in pretinfo- &gt; itagSequence. Il campo itagSequence viene spesso usato come input per il recupero di valori di colonna multivalore da un record. Tuttavia, quando si recuperano valori da un indice, è anche possibile associare la voce di indice a un numero di sequenza specifico e recuperare anche questo numero di sequenza. Il recupero del numero di sequenza può essere un'operazione dispersa e deve essere eseguito solo se necessario.</p> | 
| <p>JET_ bitRetrieveNull</p> | <p>Recupera i valori NULL della colonna multivalore. Se questa opzione non viene specificata, i valori NULL della colonna multivalore verranno ignorati automaticamente.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Fa in modo che un valore NULL sia restituito quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record. Questa opzione influisce solo sulle colonne multivalore.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Questo flag è solo per uso interno e non deve essere usato nell'applicazione.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Questo flag è solo per uso interno e non deve essere usato nell'applicazione.</p> | 



**ibLongValue**

Offset del primo byte da recuperare da una colonna di tipo JET_coltypLongBinary [o](./jet-coltyp.md) [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Numero di sequenza dei valori contenuti in una colonna multivalore. **itagSequence** qui nella **JET_RETRIEVECOLUMN** può essere 0. Se **itagSequence** è 0, viene restituito il numero di istanze di una colonna multivalore anziché i dati della colonna. Non è possibile usare un valore **itagSequence** pari a 0 nelle chiamate [a JetRetrieveColumn.](./jetretrievecolumn-function.md)

**columnidNextTagged**

Columnid **della** colonna con tag, multivalore o sparse quando tutte le colonne con tag vengono recuperate passando 0 come **columnid** [a JetRetrieveColumn.](./jetretrievecolumn-function.md)

**Err**

Codici di errore e avvisi restituiti dal recupero della colonna.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[Oggetti JetRetrieveColumns](./jetretrievecolumns-function.md)
