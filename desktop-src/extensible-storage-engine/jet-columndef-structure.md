---
description: 'Altre informazioni su: JET_COLUMNDEF Structure'
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
ms.openlocfilehash: f33823c88bf421e82d1c30d8c286f352e35ce2013451ce8353197f430107ec98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968681"
---
# <a name="jet_columndef-structure"></a>Struttura JET_COLUMNDEF


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columndef-structure"></a>Struttura JET_COLUMNDEF

La **JET_COLUMNDEF** struttura definisce i dati che possono essere archiviati in una colonna.

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

Dimensioni della struttura, in byte. Deve essere impostato su sizeof( JET_COLUMNDEF).

**columnid**

Riservato. **columnid** deve essere impostato su 0 (zero).

**coltyp**

Tipo della colonna, ad esempio testo, binario o numerico. Per altre informazioni, [vedere](./jet-coltyp.md)JET_COLTYP .

**wCountry**

Riservato. **wCountry** deve essere impostato su 0 (zero).

**langid**

Obsoleta. **langid** deve essere impostato su 0 (zero).

**cp**

Tabella codici per la colonna. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore zero indica che verrà usato il valore predefinito (inglese, 1252). Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.

**wCollate**

Riservato. **wCollate** deve essere impostato su 0 (zero).

**cbMax**

Lunghezza massima, in byte, di una colonna a lunghezza variabile o lunghezza di una colonna a lunghezza fissa.

**grbit**

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più dei valori seguenti.

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
<td><p>La colonna verrà fissata. Userà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna. JET_bitColumnFixed non può essere usato con JET_bitColumnTagged. Questo bit non può essere usato con valori long (ovvero JET_coltypLongText <strong>e</strong> <strong>JET_coltypLongBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La colonna verrà contrassegnata con tag. Le colonne contrassegnate non accettano spazio nel database se non contengono dati. Questo bit non può essere usato con JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La colonna non deve mai essere impostata su un valore NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>La colonna è una colonna versione che specifica la versione della riga. Il valore di questa colonna inizia da zero e verrà incrementato automaticamente per ogni aggiornamento nella riga.</p>
<p>Questo bit può essere applicato solo <strong>JET_coltypLong</strong> colonne. Questo bit non può essere usato con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate o JET_bitColumnTagged.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La colonna verrà incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. I numeri, tuttavia, potrebbero non essere continui. Se, ad esempio, vengono inserite cinque righe in una tabella, la colonna autoincrement potrebbe contenere i valori &quot; &quot; { 1, 2, 6, 7, 8 }. Questo bit può essere usato solo in colonne di <strong>tipo JET_coltypLong</strong> <strong>o JET_coltypCurrency</strong>.</p>
<p><strong>Windows 2000:</strong> In Windows 2000, questo bit può essere usato solo in colonne di <strong>tipo JET_coltypLong</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Questo bit è valido solo per le chiamate <a href="gg269215(v=exchg.10).md">a JetGetColumnInfo.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Questo bit è valido solo per le chiamate <a href="gg294118(v=exchg.10).md">a JetOpenTable.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Questo bit è valido solo per le chiamate <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La colonna può essere multivalore. A una colonna multivalore possono essere associati zero, uno o più valori. I vari valori in una colonna multivalore sono identificati da un numero denominato <strong>membro itagSequence,</strong> che appartiene a varie strutture, tra <a href="gg294049(v=exchg.10).md">cui: JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>e <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Le colonne multivalore devono essere colonne con tag. non possono essere colonne a lunghezza fissa o a lunghezza variabile.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Specifica che una colonna è una colonna di aggiornamento del deposito. Una colonna di aggiornamento del deposito può essere aggiornata contemporaneamente da sessioni diverse con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manterrà la coerenza transazionale. Anche una colonna di aggiornamento del deposito deve soddisfare le condizioni seguenti:</p>
<ul>
<li><p>È possibile creare una colonna di aggiornamento del deposito solo quando la tabella è vuota.</p></li>
</ul>
<ul>
<li><p>Una colonna di aggiornamento del deposito deve essere di <strong>tipo JET_coltypLong</strong>.</p></li>
</ul>
<ul>
<li><p>Una colonna di aggiornamento del deposito deve avere un valore predefinito , ovvero <strong>cbDefault</strong> deve essere positivo.</p></li>
</ul>
<ul>
<li><p>JET_bitColumnEscrowUpdate può essere usato in combinazione con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La colonna verrà creata in un oggetto senza informazioni sulla versione. Ciò significa che le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. Questo bit è utile solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Non può essere usato all'interno di una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Riservato per utilizzi futuri.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Usare JET_bitColumnDeleteOnZero invece di JET_bitColumnFinalize. JET_bitColumnFinalize possibile finalizzare una colonna. Quando una colonna che può essere finalizzata ha una colonna di aggiornamento del deposito che raggiunge zero, la riga verrà eliminata. Le versioni future potrebbero richiamare invece una funzione di callback (per altre informazioni, <a href="gg294098(v=exchg.10).md">vedere JET_CALLBACK</a>). Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito. JET_bitColumnFinalize non può essere usato con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Il valore predefinito per una colonna verrà fornito da una funzione di callback. Vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. Se si specifica JET_bitColumnUserDefinedDefault, <strong>pvDefault</strong> deve puntare <a href="gg269200(v=exchg.10).md">a</a> una struttura JET_USERDEFINEDDEFAULT e <strong>cbDefault</strong> deve essere impostato su sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p>
<ul>
<li><p>JET_bitColumnUserDefinedDefault non può essere usato insieme a JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato. Un uso comune per una colonna che può essere finalizzata è quello di usarla come campo di conteggio dei riferimenti e quando il campo raggiunge zero il record viene eliminato. JET_bitColumnDeleteOnZero è correlato a JET_bitColumnFinalize. Una colonna delete-on-zero deve essere una colonna di aggiornamento del deposito. JET_bitColumnDeleteOnZero non può essere usato con JET_bitColumnFinalize. JET_bitColumnDeleteOnZero non può essere usato con colonne predefinite definite dall'utente.</p></td>
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
<td><p>Dichiarato in Esent.h.</p></td>
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
