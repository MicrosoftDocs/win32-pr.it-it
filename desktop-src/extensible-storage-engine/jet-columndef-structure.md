---
description: 'Altre informazioni su: struttura JET_COLUMNDEF'
title: Struttura JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968621"
---
# <a name="jet_columndef-structure"></a>Struttura JET_COLUMNDEF


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columndef-structure"></a>Struttura JET_COLUMNDEF

La struttura **JET_COLUMNDEF** definisce i dati che possono essere archiviati in una colonna.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni, in byte, della struttura. Deve essere impostato su sizeof (JET_COLUMNDEF).

**ColumnID**

Riservato. **ColumnID** deve essere impostato su 0 (zero).

**coltyp**

Tipo di colonna (ad esempio, testo, binario o numerico). Per ulteriori informazioni, vedere [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Riservato. **wCountry** deve essere impostato su 0 (zero).

**langid**

Obsoleta. **LangID** deve essere impostato su 0 (zero).

**cp**

Tabella codici per la colonna. Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200). Il valore zero indica che verrà utilizzato il valore predefinito (inglese, 1252). Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.

**wCollate**

Riservato. **wCollate** deve essere impostato su 0 (zero).

**cbMax**

Lunghezza massima, in byte, di una colonna a lunghezza variabile o lunghezza di una colonna a lunghezza fissa.

**grbit**

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più dei valori seguenti.

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
<td><p>JET_bitColumnFixed</p></td>
<td><p>La colonna verrà corretta. Utilizzerà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna. Non è possibile usare JET_bitColumnFixed con JET_bitColumnTagged. Non è possibile usare questo bit con valori Long (ovvero <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La colonna verrà contrassegnata con tag. Se non contengono dati, le colonne con tag non utilizzano alcuno spazio nel database. Non è possibile usare questo bit con JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La colonna non deve mai essere impostata su un valore NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>La colonna è una colonna della versione che specifica la versione della riga. Il valore di questa colonna inizia da zero e verrà incrementato automaticamente per ogni aggiornamento nella riga.</p>
<p>Questo bit può essere applicato solo a colonne <strong>JET_coltypLong</strong> . Non è possibile usare questo bit con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate o JET_bitColumnTagged.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La colonna verrà incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. I numeri, tuttavia, potrebbero non essere continui. Se, ad esempio, vengono inserite cinque righe in una tabella, la &quot; colonna AutoIncrement &quot; potrebbe contenere i valori {1, 2, 6, 7, 8}. Questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</p>
<p><strong>Windows 2000:  </strong> In Windows 2000, questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Questo bit è valido solo per le chiamate a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Questo bit è valido solo per le chiamate a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Questo bit è valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La colonna può essere multivalore. Una colonna multivalore può avere zero, uno o più valori associati. I vari valori in una colonna multivalore sono identificati da un numero denominato membro <strong>itagSequence</strong> , che appartiene a diverse strutture, tra cui: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>e <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Le colonne multivalore devono essere contrassegnate come colonne; ovvero non possono essere colonne a lunghezza fissa o a lunghezza variabile.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Specifica che una colonna è una colonna di aggiornamento del deposito. Una colonna di aggiornamento del deposito può essere aggiornata simultaneamente da diverse sessioni con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manterrà la coerenza transazionale. Una colonna di aggiornamento del deposito deve soddisfare anche le condizioni seguenti:</p>
<ul>
<li><p>Una colonna di aggiornamento del deposito è possibile creare solo se la tabella è vuota.</p></li>
</ul>
<ul>
<li><p>Una colonna di aggiornamento del deposito vincolata deve essere di tipo <strong>JET_coltypLong</strong>.</p></li>
</ul>
<ul>
<li><p>Una colonna di aggiornamento del deposito deve avere un valore predefinito, ovvero <strong>cbDefault</strong> deve essere un valore positivo.</p></li>
</ul>
<ul>
<li><p>Non è possibile usare JET_bitColumnEscrowUpdate in combinazione con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La colonna verrà creata in un oggetto senza informazioni sulla versione. Ciò significa che le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. Questo bit è utile solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Non può essere utilizzato all'interno di una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Riservato per utilizzi futuri.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Utilizzare JET_bitColumnDeleteOnZero anziché JET_bitColumnFinalize. JET_bitColumnFinalize che una colonna può essere finalizzata. Quando una colonna che può essere finalizzata ha una colonna di aggiornamento del deposito che raggiunge lo zero, la riga verrà eliminata. Le versioni future possono richiamare invece una funzione di callback. per ulteriori informazioni, vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito. Non è possibile usare JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Il valore predefinito per una colonna verrà fornito da una funzione di callback. Vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. Specificando JET_bitColumnUserDefinedDefault significa che <strong>pvDefault</strong> deve puntare a una struttura di <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p>
<ul>
<li><p>Non è possibile usare JET_bitColumnUserDefinedDefault in combinazione con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato. Un uso comune per una colonna che può essere finalizzata è usarlo come campo di conteggio dei riferimenti e quando il campo raggiunge lo zero, il record viene eliminato. JET_bitColumnDeleteOnZero è correlato JET_bitColumnFinalize. Una colonna Delete-on-zero deve essere una colonna di aggiornamento del deposito. Non è possibile usare JET_bitColumnDeleteOnZero con JET_bitColumnFinalize. Impossibile utilizzare JET_bitColumnDeleteOnZero con le colonne predefinite definite dall'utente.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
