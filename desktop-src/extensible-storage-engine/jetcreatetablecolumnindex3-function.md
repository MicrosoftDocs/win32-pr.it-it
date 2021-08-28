---
description: Altre informazioni sulla funzione JetCreateTableColumnIndex3
title: Funzione JetCreateTableColumnIndex3
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b1e22b8816f3083fdf3cf623107197bc8a06883
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985953"
---
# <a name="jetcreatetablecolumnindex3-function"></a>Funzione JetCreateTableColumnIndex3


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreatetablecolumnindex3-function"></a>Funzione JetCreateTableColumnIndex3

La **funzione JetCreateTableColumnIndex3** crea una tabella in un database ESE con un set iniziale di indici e un set iniziale di colonne da una matrice [di JET_TABLECREATE3](./jet-tablecreate3-structure.md) esistenti. La [JET_TABLECREATE3](./jet-tablecreate3-structure.md) consente di impostare una funzione di callback.

**Windows 7:** **JetCreateTableColumnIndex3** è stato introdotto nel sistema operativo Windows 7.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*Dbid*

Identificatore del database da usare per la chiamata API.

*ptablecreate*

Puntatore a una [JET_TABLECREATE3](./jet-tablecreate3-structure.md) struttura che definisce la tabella da creare. Vedere [JET_TABLECREATE3](./jet-tablecreate3-structure.md) per altri dettagli.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Impossibile risolvere la funzione di callback. È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata. Con una registrazione sufficiente abilitata, il registro eventi fornirà altri dettagli.</p> | 
| <p>JET_errCannotIndex</p> | <p>È stato effettuato un tentativo di indicizzazione su una colonna di aggiornamento del deposito o SLV (si noti che le colonne SLV sono deprecate).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Se ptablecreate- grbit specifica JET_bitTableCreateTemplateTable, ma &gt; ptablecreate- &gt; szTemplateTableName è impostato su NULL.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Una colonna esiste già.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Si è tentato di indicizzare una colonna inesistente. Anche il tentativo di indicizzare in modo condizionale una colonna inesistente può generare questo errore.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Si è tentato di aggiungere una colonna ridondante. Non deve essere presente più di una colonna di incrementale automatico e non più di una colonna di versione per tabella.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Questo errore verrà restituito se il membro <strong>ulDensity</strong> della <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> non è stata contrassegnata come tabella modello, ovvero la tabella non JET_bitTableCreateTemplateTable impostata.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>È stato effettuato un tentativo di definire due indici identici.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Si è tentato di specificare più di un indice primario per una tabella. Una tabella deve avere esattamente un indice primario. Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>È stata specificata una definizione di indice non valida. Di seguito sono riportati alcuni dei possibili motivi per la ricezione di questo errore:</p><ul><li><p>Un indice primario è condizionale, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha un set di JET_bitIndexPrimary e il membro <strong>cConditionalColumn</strong> della <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2</a> è maggiore di zero.</p></li><li><p>Windows Server 2003 e versioni successive di Windows. Tentativo di creare un indice di tupla con limiti di tupla, ma senza passare il membro <strong>ptuplelimits</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ovvero, il membro <strong>grbit</strong> della struttura JET_INDEXCREATE2 ha JET_bitIndexTupleLimits impostato, ma il puntatore <strong>ptuplelimits</strong> è NULL).</p></li><li><p>Passaggio di una definizione di chiave non valida nel <strong>membro szKey</strong> della <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura . Vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> per una descrizione delle definizioni valide.</p></li><li><p>Impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> su maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</p></li><li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> <a href="gg294082(v=exchg.10).md">di JET_INDEXCREATE2</a>). Alcune cause comuni includono il membro <strong>pidxunicode</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è NULL o l'LCID specificato nella struttura <strong>pidxunicode</strong> non è valido.</p></li><li><p>Specifica di una colonna multivalore per un indice primario.</p></li><li><p>Tentativo di indicizzare troppe colonne condizionali. Il <strong>membro cConditionalColumn</strong> della <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e versioni successive di Windows. È <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> specificata una struttura e i relativi limiti non sono supportati. Vedere la sezione osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> dati.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla non può essere univoco, ovvero il membro <em>grbit</em> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexUnique set.</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla può essere su una sola colonna, ovvero se il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha un set di JET_bitIndexTuples e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples set.</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla può essere utilizzato solo in una colonna di tipo text o Unicode. Un tentativo di indicizzare altre colonne, ad esempio le colonne binarie, genererà JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e versioni successive di Windows. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura .</p> | 
| <p>JET_errInTransaction</p> | <p>Si è tentato di creare un indice senza informazioni sulla versione durante una transazione.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Il <strong>membro cp</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore 0 indica che verrà usato il valore predefinito (inglese, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Il <strong>membro coltyp</strong> della <a href="gg269252(v=exchg.10).md">struttura JET_COLUMNCREATE</a> non è stato impostato su un tipo di colonna valido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Di seguito sono riportati alcuni motivi per cui questo errore può verificarsi:</p><ul><li><p>Il <strong>membro rgindexcreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su NULL.</p></li><li><p>Il <strong>membro rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su NULL.</p></li><li><p>Il <strong>membro cbStruct</strong> di una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è stato impostato su un valore valido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>È stata specificata una <strong>combinazione non</strong> valida di membri grbit in <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</p><p>La definizione dell'indice non è valida perché il <strong>membro grbit</strong> contiene valori incoerenti. Di seguito sono riportati alcuni possibili motivi:</p><ul><li><p>Per un indice primario è stato specificato un bit ignore, ovvero JET_bitIndexPrimary è stato passato JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un indice vuoto non ignora i membri NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexEmpty impostato, ma non JET_bitIndexIgnoreAnyNull set.</p></li><li><p>Passaggio di una <a href="gg269214(v=exchg.10).md">struttura JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit non</strong> valido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>È stato passato un ID impostazioni locali (LCID) non valido (tramite il membro <strong>lcid</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a cui punta il membro <strong>pidxunicode</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> o tramite il campo <strong>lcid</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>È stato specificato un parametro non valido. Di seguito sono riportati alcuni possibili motivi:</p><ul><li><p>Il <strong>membro rgcolumncreate</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> è NULL.</p></li><li><p>Il <strong>membro cbStruct</strong> di una delle strutture <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> specificate nel membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> non è stato impostato su sizeof( JET_COLUMNCREATE ).</p></li><li><p>Il <strong>membro cbKey</strong> di una <a href="gg294082(v=exchg.10).md">struttura JET_INDEXCREATE2</a> è impostato su zero.</p></li><li><p>Il <strong>membro cbStruct</strong> di una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof( JET_INDEXCREATE2 ).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>Il record è troppo grande. La somma del <strong>membro cbMax</strong> della struttura JET_COLUMNCREATE <a href="gg269252(v=exchg.10).md">per</a> tutte le colonne fisse non deve superare un determinato valore.</p> | 
| <p>JET_errTableDuplicate</p> | <p>La tabella esiste già.</p> | 
| <p>JET_errTooManyColumns</p> | <p>È stato effettuato un tentativo di aggiungere troppe colonne alla tabella. Una tabella non può avere più JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode. Ciò può essere causato dall'estrazione di risorse di sistema.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un elemento della struttura degli hint per lo spazio JET non era corretto o gestibile.</p> | 



#### <a name="remarks"></a>Commenti

Il nome **JetCreateTableColumnIndex3** deriva dall'ordine di creazione degli oggetti: crea prima una tabella, colonne e infine indici. **JetCreateTableColumnIndex3** crea una tabella con un set iniziale di colonne e indici. È possibile aggiungere e rimuovere colonne e indici aggiuntivi in modo dinamico con [JetAddColumn,](./jetaddcolumn-function.md) [JetDeleteColumn,](./jetdeletecolumn-function.md) [JetDeleteColumn2,](./jetdeletecolumn2-function.md) [JetCreateIndex,](./jetcreateindex-function.md) [JetCreateIndex2,](./jetcreateindex2-function.md) [JetCreateIndex3](./jetcreateindex3-function.md)e [JetDeleteIndex.](./jetdeleteindex-function.md)

Come [JetOpenTable](./jetopentable-function.md), quando l'applicazione viene eseguita usando *il tableid* restituito, in genere deve essere chiusa [con JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCreateTableColumnIndex3W</strong> (Unicode) e <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
