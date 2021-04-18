---
description: 'Altre informazioni su: funzione JetAddColumn'
title: Funzione JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316457"
---
# <a name="jetaddcolumn-function"></a>Funzione JetAddColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetaddcolumn-function"></a>Funzione JetAddColumn

La funzione **JetAddColumn** aggiunge una nuova colonna a una tabella esistente in un database ESE.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Tabella alla quale aggiungere la colonna.

*szColumnName*

Nome della colonna da aggiungere. Il nome deve soddisfare i criteri seguenti:

  - Deve avere una lunghezza inferiore a JET_cbNameMost caratteri, escluso il carattere **null** di terminazione.

  - Deve contenere solo caratteri dei set seguenti: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.

  - Non può iniziare con uno spazio.

  - Deve contenere almeno un carattere diverso dallo spazio.

*pcolumndef*

Puntatore a una struttura [JET_COLUMNDEF](./jet-columndef-structure.md) , che definisce i dati che possono essere archiviati in una colonna.

*pvDefault*

Puntatore a un buffer che contiene il valore predefinito per la colonna. La lunghezza del buffer è **cbDefault**. Se non è disponibile alcun valore predefinito, impostare **pvDefault** su **null** e **cbDefault** su zero. I valori predefiniti non possono essere maggiori di JET_cbColumnMost byte per le colonne fisse o JET_cbLVDefaultValueMost byte per i valori Long. Se un valore predefinito è maggiore, verrà troncato automaticamente.

Se *grbit* ha JET_bitColumnUserDefinedDefault set, **pvDefault** verrà interpretato come un puntatore a una struttura di [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .

*cbDefault*

Dimensione, in byte, del buffer specificato in **pvDefault**.

*pColumnID*

Puntatore a una struttura [JET_COLUMNID](./jet-columnid.md) , che, in esito positivo, riceverà l'identificatore della colonna appena creata. In caso di errore, il valore non è definito.

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
<td><p>L'operazione è stata completata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL</p></td>
<td><p>È stato effettuato un tentativo di modificare la definizione dei dati di una tabella DDL fissa. Un esempio di tabella con DDL fisso è una tabella modello.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un parametro non valido è stato passato nell'API. Alcuni esempi di parametri non validi sono:</p>
<ul>
<li><p>Il passaggio della dimensione non corretta della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> nel membro <em>cbStruct</em> .</p></li>
<li><p>Passando JET_bitColumnUserDefinedDefault, ma non impostando <strong>cbDefault</strong> su sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>È stato effettuato un tentativo di aggiungere una colonna con il bit JET_bitColumnUnversioned set, ma la sessione è attualmente in una transazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Una colonna esiste già. È stato effettuato un tentativo di aggiungere una colonna senza informazioni sulla versione e tale colonna esiste già.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableNotEmpty</p></td>
<td><p>La tabella contiene dati. Una colonna di aggiornamento del deposito può essere aggiunta solo a una tabella vuota.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Il record è troppo grande. La somma del parametro <strong>cbMax</strong> per le colonne fisse non deve superare un determinato valore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella. Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>È stato effettuato un tentativo di aggiungere una colonna ridondante. Non deve essere presente più di una colonna AutoIncrement e non più di una colonna versione per tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>Non è stato possibile risolvere la funzione di callback. È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata. Se è abilitata la registrazione sufficiente, nel registro eventi vengono forniti ulteriori dettagli.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Avviso che indica che la lunghezza massima (<strong>cbMax</strong>) di una colonna fissa o variabile è maggiore della JET_cbColumnMost. Questo limite non si applica ai valori Long (ovvero <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Un nome non valido è stato passato come <strong>szColumnName</strong>. Per ulteriori informazioni sulle restrizioni, vedere i criteri per <strong>szColumnName</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Il campo <strong>coltyp</strong> non è stato impostato su un tipo di colonna valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Il parametro <strong>CP</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200). Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaggedNotNULL</p></td>
<td><p>Non è possibile usare JET_bitColumnNotNULL con colonne con tag, Long Value o SLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>È stata specificata una combinazione non valida di <em>grbits</em> . Di seguito sono riportati alcuni dei motivi di questo errore:</p>
<ul>
<li><p>JET_bitColumnFixed è stato utilizzato in una colonna con tag, Long Value o SLV.</p></li>
<li><p>JET_bitColumnEscrowUpdate è stato utilizzato in una colonna non di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnEscrowUpdate è stato utilizzato in una colonna versione (JET_bitColumnVersion).</p></li>
<li><p>JET_bitColumnEscrowUpdate è stato usato in una colonna AutoIncrememnt (JET_bitColumnAutoincrement).</p></li>
<li><p>JET_bitColumnEscrowUpdate è stato utilizzato in una colonna che non disponeva di un valore predefinito (<strong>cbDefault</strong> era uguale a zero).</p></li>
<li><p>JET_bitColumnFinalize è stato utilizzato in una colonna che non è una colonna di aggiornamento del deposito (JET_bitColumnEscrowUpdate non è stato impostato).</p></li>
<li><p>JET_bitColumnDeleteOnZero è stato utilizzato in una colonna che non è una colonna di aggiornamento del deposito (JET_bitColumnEscrowUpdate non è stato impostato).</p></li>
<li><p>JET_bitColumnAutoincrement è stato utilizzato in una colonna che non è stata <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p>
<p><strong>Windows 2000:  </strong> Questo motivo del codice di errore viene usato solo in Windows 2000.</p>
<p>JET_bitColumnAutoincrement è stato utilizzato in una colonna non <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> né <a href="gg269213(v=exchg.10).md">JET_coltypCurrencyta</a>.</p>
<p><strong>Windows XP:  </strong> Questo motivo del codice di errore viene utilizzato in Windows XP e nei sistemi operativi successivi.</p></li>
<li><p>JET_bitColumnVersion è stato utilizzato in una colonna che non è stata <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnVersion è stato utilizzato in una colonna AutoIncrement.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnFixed.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnNotNULL.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnVersion.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnAutoincrement.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnUpdatable.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnEscrowUpdate.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnFinalize.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnDeleteOnZero.</p></li>
<li><p>JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnMaybeNull.</p></li>
<li><p>JET_bitColumnUserDefinedDefault è stato utilizzato in una colonna non contrassegnata (che è fissa o variabile).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged</p></td>
<td><p>Una colonna multivalore (JET_bitColumnMultiValued) può essere utilizzata solo in una colonna con tag o valori Long (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged</p></td>
<td><p>Si è tentato di usare una colonna con tag quando è possibile che la colonna non sia contrassegnata con tag. Alcuni dei vincoli per la disabilitazione delle colonne con tag sono:</p>
<ul>
<li><p>Una colonna di aggiornamento del deposito (JET_bitColumnEscrowUpdate) non può essere usata in una colonna con tag o valori Long (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></li>
<li><p>Una colonna AutoIncrement potrebbe non essere contrassegnata con tag.</p></li>
<li><p>Una colonna versione potrebbe non essere contrassegnata con tag.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired</p></td>
<td><p>Per questa operazione è necessario un blocco esclusivo sulla tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Avviso che indica che la lunghezza massima (<em>cbMax</em>) di una colonna fissa o variabile è maggiore della JET_cbColumnMost. Questo limite non si applica ai valori Long (ovvero <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
</tbody>
</table>


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
<td><p>Implementato come <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
