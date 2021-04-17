---
description: 'Altre informazioni su: struttura JET_OPENTEMPORARYTABLE'
title: Struttura JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
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
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345856"
---
# <a name="jet_opentemporarytable-structure"></a>Struttura JET_OPENTEMPORARYTABLE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_opentemporarytable-structure"></a>Struttura JET_OPENTEMPORARYTABLE

La struttura **JET_OPENTEMPORARYTABLE** contiene una raccolta di parametri facilmente estendibile per la funzione di **JET_OPENTEMPORARYTABLE** . Questa struttura è la tabella temporanea equivalente della struttura [JET_TABLECREATE](./jet-tablecreate-structure.md) .

**Windows Vista:** La struttura **JET_OPENTEMPORARYTABLE** è stata introdotta in Windows Vista.

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni in byte della struttura (per l'espansione futura). Deve essere impostato su sizeof (JET_TABLECREATE) in byte.

**prgcolumndef**

Definizioni di colonna per le colonne create nella tabella temporanea.

Sono presenti **importanti** limitazioni per le opzioni di definizione di colonna utilizzate con una tabella temporanea. Per altre informazioni, vedere la sezione Osservazioni.

Oltre alle normali opzioni di definizione di colonna, è possibile specificare anche zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Il tipo di ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente. Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>La colonna sarà una colonna chiave per la tabella temporanea.</p>
<p>L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via. Se sono richieste più colonne chiave che possono essere supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</p></td>
</tr>
</tbody>
</table>


**CColumn**

Vedere *prgcolumndef*.

**pidxunicode**

ID delle impostazioni locali e flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.

Quando questo parametro non è presente e quando il parametro *LCID* non è presente, viene utilizzato il valore LCID predefinito per confrontare eventuali colonne chiave Unicode nella tabella temporanea. Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti).

Quando questo parametro non è presente, i flag di normalizzazione predefiniti verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**grbit**

Gruppo di bit che specifica zero o più delle opzioni seguenti.

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
<td><p>JET_bitTTIndexed</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</p>
<p>Se questa funzionalità non è necessaria, è consigliabile non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUnique</p></td>
<td><p>Richiede la rimozione dei record con chiavi di indice duplicate dal set di record finale nella tabella temporanea.</p>
<p>Prima di Windows Server 2003, il motore di database presuppone sempre che questa opzione sia attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci. A partire da Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</p>
<p>Non è possibile stabilire quale duplicato avrà esito positivo e quali duplicati verranno rimossi, in generale. Tuttavia, quando viene richiesta l'opzione JET_bitTTErrorOnDuplicateInsertion, il primo record con una chiave di indice specificata da inserire nella tabella temporanea avrà sempre esito positivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Richiede che la tabella temporanea sia sufficientemente flessibile da consentire la modifica successiva dei record inseriti in precedenza. Se questa funzionalità non è necessaria, è consigliabile non richiederla.</p>
<p>Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi arbitraria dei record in ordine e direzione arbitrari usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Se questa funzionalità non è necessaria, è consigliabile non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Richiede che i valori della colonna chiave <strong>null</strong> siano ordinati più vicino alla fine dell'indice rispetto ai valori di colonna chiave non null.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Impone al gestore tabelle temporaneo di abbandonare la ricerca della strategia migliore per utilizzare la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Eventuali tentativi di inserire un record con la stessa chiave di indice di un record inserito in precedenza avranno immediatamente esito negativo con JET_errKeyDuplicate. Se questa opzione non è richiesta, un duplicato viene rilevato immediatamente e non riesce o viene rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea, in base alla funzionalità richiesta.</p>
<p>Se questa funzionalità non è necessaria, è consigliabile non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>La tabella temporanea viene creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query. Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</p>
<p>Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate. Per ulteriori informazioni, vedere JET_bitTTUnique.</p>
<p><strong>Windows Server 2003:  </strong> Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p></td>
</tr>
</tbody>
</table>


**prgcolumnid**

Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.

Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.

**cbKeyMost**

Dimensione massima di una chiave che rappresenta una determinata riga.

È possibile impostare la dimensione massima della chiave per controllare la modalità di troncamento delle chiavi. Il troncamento della chiave è importante perché può influire sul fatto che le righe siano considerate distinte.

Se questo parametro è impostato su 0 o JET_cbKeyMostMin (255), le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003 e dalle versioni precedenti. Questo parametro può essere impostato anche su un valore maggiore come funzione delle dimensioni della pagina del database per l'istanza (JET_paramDatabasePageSize). Per ulteriori informazioni, vedere JET_paramKeyMost.

**cbVarSegMac**

Quantità massima di dati che verranno utilizzati da qualsiasi colonna a lunghezza variabile per costruire una chiave per una determinata riga.

Questo parametro può essere utilizzato per controllare la quantità di spazio chiave utilizzata da una determinata colonna chiave. Questo limite è in byte. Se questo parametro è zero o è uguale al parametro *cbKeyMost* , non è attivo alcun limite.

**TableID**

Handle di tabella per la tabella temporanea creata in seguito a una chiamata riuscita a [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

### <a name="requirements"></a>Requisiti

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Parametri di sistema Extensible Storage Engine](./extensible-storage-engine-system-parameters.md)
