---
description: 'Altre informazioni su: funzione JetCreateIndex4W'
title: Funzione JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315631"
---
# <a name="jetcreateindex4w-function"></a>Funzione JetCreateIndex4W


_**Si applica a:** Windows | Windows Server_

La funzione **JetCreateIndex4W** crea indici sui dati in un database Extensible Storage Engine (ESE), che può essere usato per individuare rapidamente dati specifici.

La funzione **JetCreateIndex4W** è stata introdotta nel sistema operativo Windows 8.

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Tabella in cui verrà creato l'indice.

*pindexcreate*

Matrice di strutture di [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , ognuna delle quali definisce un indice da creare.

*cIndexCreate*

Numero di elementi nella matrice *pindexcreate* .

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

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
<td><p>JET_errCannotIndex</p></td>
<td><p>È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna di aggiornamento del deposito o di una colonna SLV. si noti che le colonne SLV sono deprecate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna inesistente. Un tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Questo errore viene restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>È stato eseguito un tentativo di definire due indici identici.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>È stato effettuato un tentativo di specificare più di un indice primario per una tabella. Una tabella deve avere esattamente un indice primario. Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>È stata specificata una definizione di indice non valida. Di seguito sono riportate alcune possibili cause di questo errore:</p>
<ul>
<li><p>Un indice primario è condizionale (il membro<strong>grbit</strong> del <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha <strong>JET_bitIndexPrimary</strong> set e il membro <strong>cConditionalColumn</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è maggiore di zero).</p></li>
<li><p>Si applica alle versioni di Windows a partire da Windows Server 2003. È stato effettuato un tentativo di creare un indice di tupla con limiti di tupla, ma senza passare le informazioni nel membro <strong>ptuplelimits</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , ovvero <em>grbit</em> ha impostato <strong>JET_bitIndexTupleLimits</strong> , ma il puntatore <strong>ptuplelimits</strong> è null.</p></li>
<li><p>Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Per informazioni sulle definizioni valide, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> su un valore maggiore di <strong>JET_cbPrimaryKeyMost</strong> (per un indice primario) o maggiore di <strong>JET_cbSecondaryKeyMost</strong> (per un indice secondario).</p></li>
<li><p>Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit <strong>JET_bitIndexUnicode</strong> impostato nel membro <strong>grbit</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Alcune cause comuni possono essere che il campo pidxunicode della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è null o che l'identificatore LCID specificato nella struttura pidxunicode non è valido.</p></li>
<li><p>Specifica di una colonna multivalore per un indice primario.</p></li>
<li><p>Tentativo di indicizzare un numero eccessivo di colonne condizionali. Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di <strong>JET_ccolKeyMost</strong>.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati. Per ulteriori informazioni, vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non può essere univoco (<em>grbit</em> non deve avere sia <strong>JET_bitIndexTuples</strong> che <strong>JET_bitIndexUnique</strong> impostato).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla può trovarsi solo su una singola colonna, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone di <strong>JET_bitIndexTuples</strong> set e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia <strong>JET_bitIndexPrimary</strong> che <strong>JET_bitIndexTuples</strong> impostato).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode. Il tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà la <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Si applica alle versioni di Windows a partire da Windows XP. Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>È stato effettuato un tentativo di creare un indice senza informazioni sulla versione in una transazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>La definizione dell'indice non è valida perché il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene valori incoerenti. Di seguito sono riportati alcuni dei possibili motivi:</p>
<ul>
<li><p>Per un indice primario è stato specificato un bit ignoto (JET_bitIndexPrimary è stato passato con una delle <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>o <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li>
<li><p>Un indice vuoto non ignora alcun campo null, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha <strong>JET_bitIndexEmpty</strong> set, ma non ha <strong>JET_bitIndexIgnoreAnyNull</strong> set.</p></li>
<li><p>Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido. Vedere <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>Quando si creano più indici contemporaneamente (ovvero se il parametro <em>cIndexCreate</em> è maggiore di uno), nessuno degli indici può contenere uno dei bit seguenti:</p>
<ul>
<li><p><strong>JET_bitIndexPrimary</strong></p></li>
<li><p><strong>JET_bitIndexUnversioned</strong></p></li>
<li><p><strong>JET_bitIndexEmpty</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , che il membro <strong>pidxunicode</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene un puntatore a oppure tramite il membro <strong>LCID</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>È stato specificato un nome di indice non valido. Per ulteriori informazioni, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un parametro non valido è stato passato nell'API. Di seguito sono riportati alcuni dei motivi per cui può essere restituito questo errore:</p>
<ul>
<li><p>Il campo <strong>cbKey</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su zero.</p></li>
<li><p>Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof (JET_INDEXCREATE2).</p></li>
</ul></td>
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

La funzione **JetCreateIndex4W** scorre gli indici specificati nel parametro *pindexcreate* e talvolta si interrompe al primo errore. Eventuali indici dopo il primo indice con un errore potrebbero non essere stati tentati, anche se il membro **Err** della struttura [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contiene JET_errSuccess.

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

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
