---
description: 'Altre informazioni su: funzione JetCreateTableColumnIndex2'
title: JetCreateTableColumnIndex2 (funzione)
TOCTitle: JetCreateTableColumnIndex2 Function
ms:assetid: ad9caaf3-8cd2-453f-894d-8ac438c50b73
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294057(v=EXCHG.10)
ms:contentKeyID: 32765672
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex2W
- JetCreateTableColumnIndex2
- JetCreateTableColumnIndex2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51a1789fe050ddd62990f6561ddeb01363d69f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058337"
---
# <a name="jetcreatetablecolumnindex2-function"></a>JetCreateTableColumnIndex2 (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreatetablecolumnindex2-function"></a>JetCreateTableColumnIndex2 (funzione)

La funzione **JetCreateTableColumnIndex2** crea una tabella in un database ESE con un set iniziale di indici e un set iniziale di colonne da una matrice di strutture di [JET_TABLECREATE2](./jet-tablecreate2-structure.md) . La struttura di [JET_TABLECREATE2](./jet-tablecreate2-structure.md) consente di specificare una funzione di callback.

**Windows XP: JetCreateTableColumnIndex2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex2(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE2* ptablecreate
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*dbid*

Identificatore del database da usare per la chiamata API.

*ptablecreate*

Puntatore a una struttura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) che definisce la tabella da creare. Per ulteriori informazioni, vedere [JET_TABLECREATE2](./jet-tablecreate2-structure.md) .

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

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
<td><p>Se ptablecreate- &gt; grbit specifica JET_bitTableCreateTemplateTable, ma ptablecreate- &gt; szTemplateTableName è impostato su null.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Una colonna esiste già.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna non esistente. Il tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>È stato effettuato un tentativo di aggiungere una colonna ridondante. Non deve essere presente più di una colonna AutoIncrement e non più di una colonna versione per tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Questo errore viene restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è impostato su un numero minore di 20 o maggiore di 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> non è stata contrassegnata come tabella modello (ovvero la tabella non dispone di JET_bitTableCreateTemplateTable impostato).</p></td>
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
<td><p>È stata specificata una definizione di indice non valida. Di seguito sono riportati alcuni dei possibili motivi per la ricezione di questo errore:</p>
<ul>
<li><p>Un indice primario è condizionale (ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexPrimary set e il membro <strong>cConditionalColumn</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è maggiore di zero).</p></li>
<li><p>Windows Server 2003 e versioni successive. Il tentativo di creare un indice di tupla con limiti di tupla, ma senza passare il membro <strong>ptuplelimits</strong> nella struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_BITINDEXTUPLELIMITS set, ma il puntatore <strong>ptuplelimits</strong> è null).</p></li>
<li><p>Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Per una descrizione delle definizioni valide, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></li>
<li><p>L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> su un valore maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</p></li>
<li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> di <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Alcune cause comuni includono il membro <strong>pidxunicode</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è null o l'LCID specificato nella struttura <strong>pidxunicode</strong> non è valido.</p></li>
<li><p>Specifica di una colonna multivalore per un indice primario.</p></li>
<li><p>Tentativo di indicizzare un numero eccessivo di colonne condizionali. Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve essere maggiore di JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP e versioni successive. È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati. Vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP e versioni successive. Un indice di tupla non può essere univoco, ovvero il membro <em>grbit</em> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexUnique impostato).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP e versioni successive. Un indice della tupla può trovarsi solo su una singola colonna, ovvero se il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> dispone di JET_bitIndexTuples set e il membro <strong>szKey</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> specifica più di una colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP e versioni successive. Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples impostato).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP e versioni successive. Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode. Il tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà la JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP e versioni successive. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></td>
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
<td><p>Di seguito sono riportati alcuni dei motivi per cui questo errore può verificarsi:</p>
<ul>
<li><p>Il membro <strong>rgindexcreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</p></li>
<li><p>Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</p></li>
<li><p>Il membro <strong>cbStruct</strong> di una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non è stato impostato su un valore valido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>In <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>è stata specificata una combinazione non valida di membri <strong>grbit</strong> .</p>
<p>La definizione dell'indice non è valida perché il membro <strong>grbit</strong> contiene valori incoerenti. Di seguito sono riportate alcune possibili cause:</p>
<ul>
<li><p>Per un indice primario è stato specificato un bit Ignore (ovvero, JET_bitIndexPrimary è stato passato con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Un indice vuoto non ignora i membri NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexEmpty impostato, ma non ha JET_bitIndexIgnoreAnyNull set.</p></li>
<li><p>Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a cui fa riferimento il membro <strong>pidxunicode</strong> nella struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> o tramite il campo <strong>LCID</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>È stato specificato un parametro non valido. Di seguito sono riportate alcune possibili cause:</p>
<ul>
<li><p>Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è null.</p></li>
<li><p>Il membro <strong>cbStruct</strong> di una delle strutture <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> fornite nel membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> non è stato impostato su sizeof (JET_COLUMNCREATE).</p></li>
<li><p>Il membro <strong>cbKey</strong> di una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è impostato su zero.</p></li>
<li><p>Il membro <strong>cbStruct</strong> di una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non è impostato su sizeof (JET_INDEXCREATE).</p></li>
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
<td><p>È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella. Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode. Questo problema può essere causato dall'esaurimento delle risorse di sistema.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Il nome **JetCreateTableColumnIndex2** deriva dall'ordine di creazione degli oggetti: prima crea una tabella, le colonne e infine gli indici. **JetCreateTableColumnIndex2** crea una tabella con un set iniziale di colonne e indici. Altre colonne e indici possono essere aggiunti e rimossi dinamicamente con [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md).

Come [JetOpenTable](./jetopentable-function.md), quando l'applicazione viene eseguita utilizzando il *TableID* restituito, in genere deve essere chiuso con [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetCreateTableColumnIndex2W</strong> (Unicode) e <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
