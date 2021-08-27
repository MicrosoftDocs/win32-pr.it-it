---
description: 'Altre informazioni su: JET_OPENTEMPORARYTABLE struttura'
title: JET_OPENTEMPORARYTABLE struttura
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
ms.openlocfilehash: ee2f2ab2fca7a849f889d46badcc86a8a5438fa8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478507"
---
# <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE struttura

La **JET_OPENTEMPORARYTABLE** contiene una raccolta facilmente estendibile di parametri per la **JET_OPENTEMPORARYTABLE** funzione. Questa struttura è la tabella temporanea equivalente alla [JET_TABLECREATE](./jet-tablecreate-structure.md) struttura .

**Windows Vista:** La **JET_OPENTEMPORARYTABLE** è stata introdotta in Windows Vista.

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

Dimensioni della struttura in byte (per l'espansione futura). Deve essere impostato su sizeof( JET_TABLECREATE ) in byte.

**prgcolumndef**

Definizioni di colonna per le colonne create nella tabella temporanea.

**Esistono** limitazioni importanti per le opzioni di definizione delle colonne usate con una tabella temporanea. Per altre informazioni, vedere la sezione Osservazioni.

Oltre alle normali opzioni di definizione delle colonne, è possibile specificare zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>L'ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente. Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>La colonna sarà una colonna chiave per la tabella temporanea.</p><p>L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questa opzione impostata sarà la colonna chiave più significativa e così via. Se vengono richieste più colonne chiave di quelle supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</p> | 



**ccolumn**

Vedere *prgcolumndef.*

**pidxunicode**

ID delle impostazioni locali e flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.

Quando questo parametro non è presente e quando il *parametro lcid* non è presente, verrà utilizzato l'identificatore LCID predefinito per confrontare le colonne chiave Unicode nella tabella temporanea. L'LCID predefinito è la lingua inglese (Stati Uniti).

Quando questo parametro non è presente, verranno usati i flag di normalizzazione predefiniti per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**grbit**

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTTIndexed</p> | <p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</p><p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTUnique</p> | <p>Richiede che i record con chiavi di indice duplicate siano rimossi dal set finale di record nella tabella temporanea.</p><p>Prima di Windows Server 2003, il motore di database presupponeva sempre che questa opzione fosse attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci. A Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</p><p>Non è possibile sapere quale duplicato avrà esito positivo e quali duplicati verranno eliminati, in generale. Tuttavia, quando viene richiesta JET_bitTTErrorOnDuplicateInsertion'opzione , il primo record con una determinata chiave di indice da inserire nella tabella temporanea avrà sempre esito positivo.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Richiede che la tabella temporanea sia sufficientemente flessibile da consentire la successiva modifica dei record inseriti in precedenza. Se questa funzionalità non è necessaria, è meglio non richiederla.</p><p>Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e in direzione tramite <a href="gg294117(v=exchg.10).md">JetMove.</a></p><p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Richiede che <strong>i valori</strong> delle colonne chiave NULL si sordinamento più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Forza la gestione tabelle temporanee ad abbandonare la ricerca per la strategia migliore da usare per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con JET_errKeyDuplicate. Se questa opzione non è richiesta, un duplicato viene rilevato immediatamente e ha esito negativo o viene rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea, in base alla funzionalità richiesta.</p><p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>La tabella temporanea viene creata solo se la gestione tabelle temporanee può utilizzare l'implementazione ottimizzata per i risultati intermedi delle query. Se una caratteristica della tabella temporanea impedirebbe l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</p><p>Un effetto collaterale di questa opzione è consentire alla tabella temporanea di contenere record con chiavi di indice duplicate. Vedere JET_bitTTUnique per altre informazioni.</p><p><strong>Windows Server 2003:</strong> Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p> | 



**prgcolumnid**

Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.

Gli ID di colonna in questa matrice corrisponderanno esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni di questo buffer devono corrispondere alle dimensioni della matrice di input.

**cbKeyMost**

Dimensione massima per una chiave che rappresenta una determinata riga.

È possibile impostare le dimensioni massime delle chiavi per controllare la modalità di troncamento delle chiavi. Il troncamento delle chiavi è importante perché può influire sul momento in cui le righe vengono considerate distinte.

Se questo parametro è impostato su 0 o JET_cbKeyMostMin (255), le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003 e dalle versioni precedenti. Questo parametro può anche essere impostato su un valore maggiore come funzione delle dimensioni della pagina del database per l'istanza (JET_paramDatabasePageSize). Vedere JET_paramKeyMost per altre informazioni.

**cbVarSegMac**

Quantità massima di dati che verranno utilizzati da qualsiasi colonna a lunghezza variabile per costruire una chiave per una determinata riga.

Questo parametro può essere usato per controllare la quantità di spazio della chiave utilizzato da una determinata colonna chiave. Questo limite è in byte. Se questo parametro è zero o è uguale al *parametro cbKeyMost,* non è attivo alcun limite.

**tableid**

Handle di tabella per la tabella temporanea creata in seguito a una chiamata riuscita a [JetOpenTemporaryTable.](./jetopentemporarytable-function.md)

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[Parametri di sistema del motore Archiviazione estendibile](./extensible-storage-engine-system-parameters.md)
