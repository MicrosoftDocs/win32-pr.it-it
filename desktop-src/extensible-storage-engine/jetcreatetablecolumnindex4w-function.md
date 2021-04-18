---
description: 'Altre informazioni su: funzione JetCreateTableColumnIndex4W'
title: JetCreateTableColumnIndex4W (funzione)
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319181"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>JetCreateTableColumnIndex4W (funzione)


_**Si applica a:** Windows | Windows Server_

La funzione **JetCreateTableColumnIndex4W** crea una tabella in un motore di archiviazione estensibile (ESE, database con un set iniziale di indici e un set iniziale di colonne da una matrice di strutture di [JET_TABLECREATE3](./jet-tablecreate3-structure.md) . La struttura di [JET_TABLECREATE3](./jet-tablecreate3-structure.md) consente di specificare una funzione di callback.

La funzione **JetCreateTableColumnIndex4W** è stata introdotta nel sistema operativo Windows 8.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*dbid*

Identificatore del database da usare per la chiamata API.

*ptablecreate*

Puntatore a una struttura [JET_TABLECREATE3](./jet-tablecreate3-structure.md) che definisce la tabella da creare. Per ulteriori informazioni, vedere [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente. Per ulteriori informazioni sui possibili errori di Extensible Storage enginge (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>Non è stato possibile risolvere la funzione di callback. È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata. Con la registrazione sufficiente abilitata, nel registro eventi vengono forniti ulteriori dettagli.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna di aggiornamento del deposito o di una colonna SLV. si noti che le colonne SLV sono deprecate.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>Restituito se il parametro <em>ptablecreate- &gt; grbit</em> specifica il valore JET_bitTableCreateTemplateTable, ma il parametro <em>ptablecreate- &gt; szTemplateTableName</em> è impostato su null.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Una colonna esiste già.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna inesistente. Un tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>È stato effettuato un tentativo di aggiungere una colonna ridondante. Non deve esistere più di una colonna AutoIncrement e non deve esistere più di una colonna di versione per ogni tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Questo errore viene restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> non è stata contrassegnata come tabella modello (ovvero, per la tabella non è stato impostato il valore del parametro JET_bitTableCreateTemplateTable).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>È stato eseguito un tentativo di definire due indici identici.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>È stato effettuato un tentativo di specificare più di un indice primario per una tabella. Una tabella deve avere esattamente un indice primario. Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>È stata specificata una definizione di indice non valida. Di seguito sono riportate alcune delle possibili cause di questo errore:</p>
<ul>
<li><p>Un indice primario è condizionale (ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone del valore JET_bitIndexPrimary impostato e il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è maggiore di zero).</p></li>
<li><p>Si applica alle versioni del sistema operativo Windows Server a partire da Windows Server 2003. Tentativo di creare un indice di tupla con limiti di tupla, ma senza passare il membro <strong>ptuplelimits</strong> nella struttura di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ovvero il membro <strong>grbit</strong> della struttura <strong>JET_INDEXCREATE2</strong> ha JET_bitIndexTupleLimits set di valori, ma il puntatore <strong>ptuplelimits</strong> è null).</p></li>
<li><p>Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Per informazioni sulle definizioni valide, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> in modo che sia maggiore del valore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore del valore JET_cbSecondaryKeyMost (per un indice secondario).</p></li>
<li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit del valore JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ). Alcune cause comuni includono il membro <strong>pidxunicode</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è null o l'LCID specificato nella struttura <strong>pidxunicode</strong> non è valido.</p></li>
<li><p>Specifica di una colonna multivalore per un indice primario.</p></li>
<li><p>Tentativo di indicizzare un numero eccessivo di colonne condizionali. Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di <strong>JET_ccolKeyMost</strong>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati. Per ulteriori informazioni, vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non può essere univoco, ovvero il membro <em>grbit</em> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere set di valori JET_bitIndexPrimary e JET_bitIndexUnique).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla può trovarsi solo su una singola colonna, ovvero se il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone di JET_bitIndexTuples valore impostato e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples impostato).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode. Un tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà un JET_errIndexTuplesTextColumnsOnly codice di risposta.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>È stato effettuato un tentativo di creare un indice senza informazioni sulla versione in una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Il membro <strong>CP</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200). Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Il membro <strong>coltyp</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su un tipo di colonna valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>Di seguito sono riportati alcuni dei motivi per cui è possibile che si verifichi questo errore:</p>
<ul>
<li><p>Il membro <strong>rgindexcreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</p></li>
<li><p>Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</p></li>
<li><p>Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è stato impostato su un valore valido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Nella struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> è stata specificata una combinazione non valida di membri <strong>grbit</strong> .</p>
<p>La definizione dell'indice non è valida perché il membro <strong>grbit</strong> contiene valori incoerenti. Di seguito sono riportati alcuni dei possibili motivi:</p>
<ul>
<li><p>Per un indice primario è stato specificato un bit ignore, ovvero JET_bitIndexPrimary valore è stato passato con i valori JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull.</p></li>
<li><p>Un indice vuoto non ignora i membri null, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone del valore JET_bitIndexEmpty impostato, ma non ha JET_bitIndexIgnoreAnyNull set di valori.</p></li>
<li><p>Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a cui punta il membro <strong>pidxunicode</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> o tramite il campo <strong>LCID</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>È stato specificato un parametro non valido. Di seguito sono riportati alcuni dei possibili motivi:</p>
<ul>
<li><p>Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> è null.</p></li>
<li><p>Il membro <strong>cbStruct</strong> di una delle strutture <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> fornite nel membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> non è stato impostato su sizeof (JET_COLUMNCREATE).</p></li>
<li><p>Il membro <strong>cbKey</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su zero.</p></li>
<li><p>Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof (JET_INDEXCREATE2).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Il record è troppo grande. La somma del membro <strong>cbMax</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> per tutte le colonne fisse non deve superare un determinato valore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>La tabella esiste già.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella. Una tabella non può contenere più di <strong>JET_ccolFixedMost</strong> colonne fisse, non più di <strong>JET_ccolVarMost</strong> colonne a lunghezza variabile e non più di <strong>JET_ccolTaggedMost</strong> colonne con tag.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode. Questo problema può essere causato dall'esaurimento delle risorse di sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>Un elemento della struttura degli hint di spazio JET non è corretto o non è attivabile.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

La funzione **JetCreateTableColumnIndex4W** crea una tabella con un set iniziale di colonne e indici. È possibile aggiungere e rimuovere in modo dinamico colonne e indici aggiuntivi mediante le funzioni [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md) .

Come per la funzione [JetOpenTable](./jetopentable-function.md) , quando l'applicazione viene eseguita utilizzando il *TableID* restituito, la funzione [JetCloseTable](./jetclosetable-function.md) deve chiudere l'applicazione.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedi anche

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
