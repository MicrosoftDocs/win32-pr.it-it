---
description: 'Altre informazioni su: funzione JetCreateTable'
title: Funzione JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319184"
---
# <a name="jetcreatetable-function"></a>Funzione JetCreateTable


_**Si applica a:** Windows | Windows Server_

## <a name="jetcreatetable-function"></a>Funzione JetCreateTable

La funzione **JetCreateTable** crea una tabella vuota in un database ESE.

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da utilizzare.

*dbid*

Identificatore del database da utilizzare.

*szTableName*

Nome dell'indice da creare.

Il nome deve essere formattato in base alle regole seguenti:

  - Essere minore di JET_cbNameMost, escluso il valore NULL di terminazione.

  - Essere costituito dal set di caratteri seguente: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di " \! " (punto esclamativo), "," (virgola), " \[ " (parentesi di apertura) e " \] " (parentesi di chiusura), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c, 0x5D tramite 0x7F.

  - Non iniziare con uno spazio.

  - Essere costituito da almeno un carattere diverso dallo spazio.

*lPages*

Numero iniziale di pagine del database da allocare per la tabella. La specifica di un numero maggiore di uno può ridurre la frammentazione se nella tabella vengono inserite molte righe.

*lDensity*

Densità della tabella, in punti percentuali. Il numero deve essere 0 o compreso tra 20 e 100. Il valore 0 indica che deve essere utilizzato il valore predefinito. Il valore predefinito è 80.

*pTableID*

In seguito all'esito positivo, l'identificatore di tabella viene restituito in questo campo. Il valore non è definito se l'API non restituisce JET_errSuccess.

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
<td><p>È stata passata una densità non valida nel membro <em>ulDensity</em> della struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> non è stata contrassegnata come tabella modello (ovvero la tabella non dispone di JET_bitTableCreateTemplateTable impostato).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>È stato effettuato un tentativo di definire due indici identici.</p></td>
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
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP e versioni successive. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP e versioni successive. Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode. Il tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà la JET_errIndexTuplesTextColumnsOnly.</p></td>
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

**JetCreateTable** crea una tabella che non contiene colonne. Per aggiungere colonne, vedere [JetAddColumn](./jetaddcolumn-function.md).

Internamente, **JetCreateTable** chiama [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), compilando una struttura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) con:

  - JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)

  - JET_TABLECREATE2. szTableName = szTableName

  - JET_TABLECREATE2. ulPages = lPage

  - JET_TABLECREATE2. ulDensity = lDensity

  - JET_TABLECREATE2. TableID = JET_tableidNil

Tutti gli altri campi della struttura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) interna sono impostati su zero o null. Nell'output *pTableID* verrà impostato su JET_TABLECREATE2. TableID.

Per ulteriori informazioni, vedere [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .

Analogamente a [JetOpenTable](./jetopentable-function.md), quando l'applicazione viene eseguita utilizzando il membro **TableID** restituito dalla struttura di [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , è in genere necessario chiuderla con [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisiti

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
<td><p>Implementato come <strong>JetCreateTableW</strong> (Unicode) e <strong>JetCreateTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
