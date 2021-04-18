---
description: 'Altre informazioni su: struttura JET_COLUMNBASE'
title: Struttura JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319210"
---
# <a name="jet_columnbase-structure"></a>Struttura JET_COLUMNBASE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columnbase-structure"></a>Struttura JET_COLUMNBASE

La struttura **JET_COLUMNBASE** descrive i parametri di una colonna di base. Le funzioni [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usano la struttura **JET_COLUMNBASE** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni, in byte, della struttura. Impostare **cbStruct** su sizeof (JET_COLUMNBASE).

**ColumnID**

Riservato. Impostare **ColumnID** su 0 (zero).

**coltyp**

Tipo di colonna (ad esempio, testo, binario o numerico). Per ulteriori informazioni, vedere [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Riservato. Impostare su 0 (zero).

**langid**

Riservato. Impostare su 0 (zero).

**cp**

Tabella codici per la colonna. Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200). Il valore zero indica che verrà utilizzato il valore predefinito (inglese, 1252). Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.

**wFiller**

Riservato. Impostare su 0 (zero).

**cbMax**

Lunghezza massima, in byte, di una colonna a lunghezza variabile o lunghezza effettiva, in byte, di una colonna a lunghezza fissa.

**grbit**

Opzioni per la colonna, inclusi zero o più dei valori seguenti.

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
<td><p>La colonna è fissa e occupa la stessa quantità di spazio in una riga indipendentemente dalla quantità di dati in essa contenuti. JET_bitColumnFixed non possono essere combinati con JET_bitColumnTagged e non possono essere usati quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLongText</strong> o <strong>JET_coltypLongBinary</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La colonna è contrassegnata e occupa lo spazio nel database solo se contiene dati. Non è possibile combinare JET_bitColumnTagged con JET_bitColumnFixed, JET_bitColumnVersion o JET_bitColumnEscrowUpdate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La colonna non deve essere impostata su un valore <strong>null</strong> .</p>
<p>Non è possibile combinare JET_bitColumnNotNULL con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>La colonna è una colonna della versione che specifica la versione della riga. Il valore di questa colonna inizia da zero e viene incrementato automaticamente per ogni aggiornamento della riga.</p>
<p>JET_bitColumnVersion può essere utilizzato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong> e non può essere combinato con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged o JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La colonna viene incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. I numeri, tuttavia, non possono essere sequenziali. Se, ad esempio, vengono inserite cinque righe in una tabella, la colonna incrementata automaticamente potrebbe contenere i valori {1, 2, 6, 7, 8}.</p>
<p>JET_bitColumnAutoincrement può essere utilizzato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong> o <strong>JET_coltypCurrency</strong> e non può essere combinato con JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault o JET_bitColumnVersion.</p>
<p><strong>Windows 2000:  </strong> JET_bitColumnVersion può essere utilizzato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Valido solo per le chiamate a <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>. Non è possibile combinare JET_bitColumnUpdatable con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Valido solo per le chiamate a <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Valido solo per le chiamate a <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La colonna può essere multivalore. Una colonna multivalore può avere zero, uno o più valori associati. I vari valori in una colonna multivalore sono identificati da un numero nel membro <strong>itagSequence</strong> di varie strutture, ad esempio <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Le colonne multivalore devono essere contrassegnate come colonne; ovvero, non possono essere colonne a lunghezza fissa o a lunghezza variabile.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Specifica che una colonna è una colonna di aggiornamento del deposito che può essere aggiornata simultaneamente da sessioni diverse con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e che avrà coerenza transazionale.</p>
<ul>
<li><p>Una colonna di aggiornamento del deposito è possibile creare solo se la tabella è vuota.</p></li>
</ul>
<ul>
<li><p>Per una colonna di aggiornamento del deposito, il membro <strong>coltyp</strong> deve essere impostato su <strong>JET_coltypLong.</strong></p></li>
</ul>
<ul>
<li><p>Una colonna di aggiornamento del deposito deve avere un valore predefinito, ovvero <strong>cbDefault</strong> deve essere un valore positivo.</p></li>
</ul>
<ul>
<li><p>Non è possibile combinare JET_bitColumnEscrowUpdate con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La colonna viene creata senza un numero di versione. Ciò significa che altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. JET_bitColumnUnversioned viene utilizzata solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Non può essere utilizzato all'interno di una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Riservato per utilizzi futuri.</p>
<p>Non è possibile combinare JET_bitColumnMaybeNull con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Non usare. In alternativa, usare JET_bitColumnDeleteOnZero.</p>
<p>La colonna può essere finalizzata. Una colonna che può essere finalizzata è una colonna di aggiornamento del deposito che causa l'eliminazione della riga quando la colonna raggiunge lo zero. Le versioni future possono invece richiamare una funzione di callback (vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito. Non è possibile combinare JET_bitColumnFinalize con JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>Il valore predefinito per una colonna verrà fornito da una funzione di callback. Vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. Se JET_bitColumnUserDefinedDefault è specificato, <strong>pvDefault</strong> deve puntare a una struttura di <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof (JET_USERDEFINEDDEFAULT).</p>
<p>Non è possibile combinare JET_bitColumnUserDefinedDefault con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato. Un uso comune per le colonne Delete-on-zero è come campi del conteggio dei riferimenti. Quando il numero di riferimenti è pari a zero, il record viene eliminato. Una colonna Delete-on-zero deve essere una colonna di aggiornamento del deposito.</p>
<p>JET_bitColumnDeleteOnZero sostituisce JET_bitColumnFinalize.</p>
<p>Non è possibile combinare JET_bitColumnDeleteOnZero con JET_bitColumnFinalize o JET_bitColumnUserDefinedDefault né usare le colonne predefinite definite dall'utente.</p></td>
</tr>
</tbody>
</table>


**szBaseTableName**

Tabella da cui la tabella corrente eredita la DDL.

**szBaseColumnName**

Nome della colonna nella tabella del modello.

### <a name="remarks"></a>Commenti

**JET_COLUMNBASE** contiene gran parte delle stesse informazioni [JET_COLUMNDEF](./jet-columndef-structure.md), ma aggiunge campi stringa per descrivere la tabella di base (se è stata usata una DDL gerarchica).

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
<td><p>Implementato come <strong>JET_COLUMNBASE_W</strong> (Unicode) e <strong>JET_COLUMNBASE_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
