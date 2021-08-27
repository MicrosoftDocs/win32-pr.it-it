---
description: Altre informazioni sulla funzione JetCreateTableColumnIndex
title: Funzione JetCreateTableColumnIndex
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b17fea6bc4ee4856c3cae653eb8f138156ce9927
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986014"
---
# <a name="jetcreatetablecolumnindex-function"></a>Funzione JetCreateTableColumnIndex


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreatetablecolumnindex-function"></a>Funzione JetCreateTableColumnIndex

La **funzione JetCreateTableColumnIndex** crea una tabella in un database ESE con un set iniziale [](./jet-tablecreate-structure.md) di indici e un set iniziale di colonne da una matrice di JET_TABLECREATE strutture. Il nome **JetCreateTableColumnIndex** deriva dall'ordine di creazione degli oggetti. Crea prima una tabella, le colonne e infine gli indici.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*Dbid*

Identificatore del database da usare per la chiamata API.

*ptablecreate*

Puntatore a una [JET_TABLECREATE](./jet-tablecreate-structure.md) struttura che definisce la tabella da creare. Vedere [JET_TABLECREATE](./jet-tablecreate-structure.md) per altri dettagli.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Impossibile risolvere la funzione di callback. È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata. Con una registrazione sufficiente abilitata, il registro eventi fornirà altri dettagli.</p> | 
| <p>JET_errCannotIndex</p> | <p>È stato effettuato un tentativo di indicizzazione su una colonna escrow-update o SLV (si noti che le colonne SLV sono deprecate).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Se ptablecreate- grbit specifica JET_bitTableCreateTemplateTable, ma &gt; ptablecreate- &gt; szTemplateTableName è impostato su NULL.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Una colonna esiste già.</p> | 
| <p>JET_errColumnNotFound</p> | <p>È stato effettuato un tentativo di indicizzare una colonna inesistente. Anche il tentativo di indicizzare in modo condizionale una colonna inesistente può generare questo errore.</p> | 
| <p>JET_errColumnRedundant</p> | <p>È stato effettuato un tentativo di aggiungere una colonna ridondante. Non deve essere presente più di una colonna autoincrement e non più di una colonna di versione per ogni tabella.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Questo errore verrà restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è impostato su un numero minore di 20 o maggiore di 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> non è stata contrassegnata come tabella modello, ovvero la tabella non JET_bitTableCreateTemplateTable impostata.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>È stato effettuato un tentativo di definire due indici identici.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>È stato effettuato un tentativo di specificare più di un indice primario per una tabella. Una tabella deve avere esattamente un indice primario. Se non viene specificato alcun indice primario, il motore di database ne creerà in modo trasparente uno.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>È stata specificata una definizione di indice non valida. Alcuni dei possibili motivi per la ricezione di questo errore sono:</p><ul><li><p>Un indice primario è condizionale, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexPrimary impostato e il membro <strong>cConditionalColumn</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è maggiore di zero.</p></li><li><p>Windows Server 2003 e versioni successive. Tentativo di creare un indice di tupla con limiti di tupla, ma senza passare il membro <strong>ptuplelimits</strong> nella struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ,ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexTupleLimits impostato, ma il puntatore <strong>ptuplelimits</strong> è NULL.</p></li><li><p>Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> struttura . Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per una descrizione delle definizioni valide.</p></li><li><p>L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> deve essere maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</p></li><li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> <a href="gg269186(v=exchg.10).md">di JET_INDEXCREATE</a>). Alcune cause comuni includono il membro <strong>pidxunicode</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è NULL o l'LCID specificato nella struttura <strong>pidxunicode</strong> non è valido.</p></li><li><p>Specifica di una colonna multivalore per un indice primario.</p></li><li><p>Tentativo di indicizzare troppe colonne condizionali. Il <strong>membro cConditionalColumn</strong> della <a href="gg269186(v=exchg.10).md">struttura JET_INDEXCREATE</a> non deve essere maggiore di JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP e versioni successive. È <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> specificata una struttura e i relativi limiti non sono supportati. Vedere la sezione osservazioni della <a href="gg269207(v=exchg.10).md">struttura</a> JET_TUPLELIMITS.</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla non può essere univoco, ovvero il membro <em>grbit</em> della struttura JET_INDEXCREATE non deve avere sia JET_bitIndexPrimary che JET_bitIndexUnique set. <a href="gg269186(v=exchg.10).md"></a></p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla può essere solo su una singola colonna, ovvero se il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha un set di JET_bitIndexTuples e il membro <strong>szKey</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> specifica più colonne.</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples set.</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP e versioni successive. Un indice di tupla può essere solo in una colonna di tipo text o Unicode. Un tentativo di indicizzare altre colonne, ad esempio colonne binarie, genererà JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP e versioni successive. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> struttura .</p> | 
| <p>JET_errInTransaction</p> | <p>È stato effettuato un tentativo di creare un indice senza informazioni sulla versione durante una transazione.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Il <strong>membro cp</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore 0 indica che verrà usato il valore predefinito (inglese, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Il <strong>membro coltyp</strong> della <a href="gg269252(v=exchg.10).md">struttura JET_COLUMNCREATE</a> non è stato impostato su un tipo di colonna valido.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Alcuni dei motivi per cui questo errore può verificarsi:</p><ul><li><p>Il <strong>membro rgindexcreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su NULL.</p></li><li><p>Il <strong>membro rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su NULL.</p></li><li><p>Il <strong>membro cbStruct</strong> di una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non è stato impostato su un valore valido.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>È stata specificata una combinazione non valida di membri <strong>grbit</strong> in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</p><p>La definizione dell'indice non è valida perché il <strong>membro grbit</strong> contiene valori incoerenti. Alcuni motivi possibili sono:</p><ul><li><p>Per un indice primario è stato specificato un bit ignore, ovvero JET_bitIndexPrimary è stato passato JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un indice vuoto non ignora i membri NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexEmpty impostato, ma non JET_bitIndexIgnoreAnyNull set.</p></li><li><p>Passaggio di una <a href="gg269214(v=exchg.10).md">struttura JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit non</strong> valido.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>È stato passato un ID impostazioni locali (LCID) non valido (tramite il membro <strong>lcid</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a cui punta il membro <strong>pidxunicode</strong> nella struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> o tramite il campo <strong>lcid</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE).</a></p> | 
| <p>JET_errInvalidParameter</p> | <p>È stato specificato un parametro non valido. Alcuni motivi possibili sono:</p><ul><li><p>Il <strong>membro rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è NULL.</p></li><li><p>Il <strong>membro cbStruct</strong> di una delle strutture <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> specificate nel membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> non è stato impostato su sizeof( JET_COLUMNCREATE).</p></li><li><p>Il <strong>membro cbKey</strong> di una <a href="gg269186(v=exchg.10).md">struttura JET_INDEXCREATE</a> è impostato su zero.</p></li><li><p>Il <strong>membro cbStruct</strong> di una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non è impostato su sizeof( JET_INDEXCREATE).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>Il record è troppo grande. La somma del <strong>membro cbMax</strong> della <a href="gg269252(v=exchg.10).md">struttura</a> JET_COLUMNCREATE per tutte le colonne fisse non deve superare un determinato valore.</p> | 
| <p>JET_errTableDuplicate</p> | <p>La tabella esiste già.</p> | 
| <p>JET_errTooManyColumns</p> | <p>È stato effettuato un tentativo di aggiungere troppe colonne alla tabella. Una tabella non può avere più JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode. Questo problema può essere causato dall'estrazione di risorse di sistema.</p> | 



#### <a name="remarks"></a>Commenti

La chiamata di **JetCreateTableColumnIndex** è identica alla chiamata di [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), con ogni campo nella struttura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) contenente il valore del campo corrispondente [di JET_TABLECREATE](./jet-tablecreate-structure.md), con le eccezioni seguenti:

  - JET_TABLECREATE2.cbStruct impostato su sizeof( JET_TABLECREATE2)

  - JET_TABLECREATE2.szCallback impostato su NULL

  - JET_TABLECREATE2.cbtyp impostato su 0

Per [altre informazioni, vedere JetCreateTableColumnIndex2.](./jetcreatetablecolumnindex2-function.md)

Analogamente [a JetOpenTable](./jetopentable-function.md), quando l'applicazione viene eseguita usando *il tableid* restituito, in genere deve essere chiusa [con JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetCreateTableColumnIndexW</strong> (Unicode) e <strong>JetCreateTableColumnIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex]()  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
