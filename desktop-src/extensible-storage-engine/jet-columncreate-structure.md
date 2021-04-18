---
description: 'Altre informazioni su: struttura JET_COLUMNCREATE'
title: Struttura JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315153"
---
# <a name="jet_columncreate-structure"></a>Struttura JET_COLUMNCREATE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columncreate-structure"></a>Struttura JET_COLUMNCREATE

La struttura **JET_COLUMNCREATE** descrive una colonna da creare in un database.

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni, in byte, della struttura. Questo campo deve essere inizializzato su **sizeof (JET_COLUMNCREATE)**.

**szColumnName**

Nome della colonna da creare. Il nome deve soddisfare i criteri seguenti:

  - Deve avere una lunghezza inferiore a JET_cbNameMost caratteri, escluso il carattere NULL di terminazione.

<!-- end list -->

  - Deve contenere solo caratteri dei set seguenti: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c, 0x5D tramite 0x7F.

<!-- end list -->

  - Non può iniziare con uno spazio.

<!-- end list -->

  - Deve contenere almeno un carattere diverso dallo spazio.

**coltyp**

Tipo di colonna (ad esempio, testo, binario o numerico). Per ulteriori informazioni, vedere [JET_COLTYP](./jet-coltyp.md).

**cbMax**

Lunghezza massima, in byte, di una colonna a lunghezza variabile. Lunghezza della colonna per le colonne a lunghezza fissa.

**grbit**

Gruppo di bit che contengono le opzioni per la struttura e che includono zero o più dei valori seguenti.

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
<td><p>La colonna è fissa. Utilizzerà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna. Non è possibile usare JET_bitColumnFixed con JET_bitColumnTagged. Non è possibile usare questo bit con valori Long, ad esempio <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La colonna è contrassegnata con tag. Se non contengono dati, le colonne con tag non utilizzano alcuno spazio nel database. Non è possibile usare questo bit con JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La colonna non deve mai essere impostata su un valore NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La colonna viene incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. Il numero, tuttavia, potrebbe non essere continuo. Se, ad esempio, vengono inserite cinque righe in una tabella, la colonna AutoIncrement potrebbe contenere i valori {1, 2, 6, 7, 8}.</p>
<p><strong>Windows 2000:  </strong> Questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong>.</p>
<p><strong>Windows Server 2003 e versioni successive:  </strong> Questo bit può essere utilizzato solo su colonne di tipo <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Questo bit è valido solo per le chiamate a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Questo bit è valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Questo bit è valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La colonna può essere multivalore. Una colonna multivalore può avere zero, uno o più valori associati. I vari valori in una colonna multivalore sono identificati dal membro <strong>itagSequence</strong> di varie strutture, ad esempio <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Le colonne multivalore devono essere contrassegnate come colonne; ovvero non possono essere colonne a lunghezza fissa o a lunghezza variabile.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>La colonna è una colonna di aggiornamento del deposito. Una colonna di aggiornamento del deposito può essere aggiornata simultaneamente da diverse sessioni con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e mantenere la coerenza delle transazioni.</p>
<ul>
<li><p>Una colonna di aggiornamento del deposito è possibile creare solo se la tabella è vuota.</p></li>
<li><p>Una colonna di aggiornamento del deposito vincolata deve essere di tipo <strong>JET_coltypLong.</strong></p></li>
<li><p>Una colonna di aggiornamento del deposito deve avere un valore predefinito, ovvero <strong>cbDefault</strong> deve essere un valore positivo.</p></li>
<li><p>Non è possibile usare JET_bitColumnEscrowUpdate insieme alle costanti seguenti:</p>
<ul>
<li><p>JET_bitColumnTagged</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La colonna viene creata senza una versione. Le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. Questo bit è utile solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Non può essere utilizzato all'interno di una transazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Riservato per utilizzi futuri.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Utilizzare JET_bitColumnDeleteOnZero anziché JET_bitColumnFinalize. JET_bitColumnFinalize specifica che una colonna può essere finalizzata. Quando una colonna che può essere finalizzata ha una colonna di aggiornamento del deposito che raggiunge lo zero, la riga verrà eliminata. Le versioni future possono invece richiamare una funzione di callback. Per ulteriori informazioni, vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito. Non è possibile usare JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Il valore predefinito per una colonna viene fornito dalla funzione di callback <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. <strong>pvDefault</strong> deve puntare a una struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p>
<p>Non è possibile usare JET_bitColumnUserDefinedDefault insieme alle costanti seguenti:</p>
<ul>
<li><p>JET_bitColumnFixed</p></li>
<li><p>JET_bitColumnNotNULL</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
<li><p>JET_bitColumnUpdatable</p></li>
<li><p>JET_bitColumnEscrowUpdate</p></li>
<li><p>JET_bitColumnFinalize</p></li>
<li><p>JET_bitColumnDeleteOnZero</p></li>
<li><p>JET_bitColumnMaybeNull</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato. Un uso comune per una colonna che può essere finalizzata è usarlo come campo di conteggio dei riferimenti e quando il campo raggiunge lo zero, il record viene eliminato. JET_bitColumnDeleteOnZero è correlato JET_bitColumnFinalize. Una colonna Delete-on-zero deve essere una colonna di aggiornamento del deposito. Non è possibile usare JET_bitColumnDeleteOnZero con JET_bitColumnFinalize. Impossibile utilizzare JET_bitColumnDeleteOnZero con le colonne predefinite definite dall'utente.</p></td>
</tr>
</tbody>
</table>


**pvDefault**

Punta a un buffer che sarà il valore predefinito per una colonna. La lunghezza del buffer è **cbDefault**. Se non è disponibile alcun valore predefinito, **pvDefault** deve essere impostato su null e **cbDefault** deve essere impostato su zero. Se *grbit* ha JET_bitColumnUserDefinedDefault set, **pvDefault** verrà interpretato come un puntatore a una struttura di JET_USERDEFINEDDEFAULT. I valori predefiniti non possono essere superiori a 255 byte. Se un valore predefinito è maggiore di 255 byte, verrà troncato automaticamente.

**cbDefault**

Dimensione, in byte, del buffer specificato da **pvDefault**.

**cp**

Tabella codici per la colonna. Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200). Il valore zero indica che verrà utilizzato il valore predefinito (inglese, 1252). Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.

**ColumnID**

In seguito all'esito positivo, l'identificatore di colonna della colonna appena creata verrà passato nuovamente in questo campo. In caso di errore, il valore non è definito.

**Err**

Il campo **Err** conterrà lo stato della creazione della colonna. Per un elenco dei valori restituiti probabili, vedere [JetAddColumn](./jetaddcolumn-function.md) .

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_COLUMNCREATE_W</strong> (Unicode) e <strong>JET_COLUMNCREATE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
