---
description: 'Altre informazioni su: JET_COLUMNCREATE Structure'
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
ms.openlocfilehash: ffe79dde0f24e82aa7ca9457604ea76b587e9b29
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984024"
---
# <a name="jet_columncreate-structure"></a>Struttura JET_COLUMNCREATE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columncreate-structure"></a>Struttura JET_COLUMNCREATE

La **JET_COLUMNCREATE** struttura descrive una colonna da creare in un database.

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

Dimensioni della struttura, in byte. Questo campo deve essere inizializzato su **sizeof( JET_COLUMNCREATE )**.

**szColumnName**

Nome della colonna da creare. Il nome deve soddisfare i criteri seguenti:

  - La lunghezza deve essere inferiore JET_cbNameMost caratteri, senza includere il carattere di terminazione NULL.

<!-- end list -->

  - Deve contenere caratteri solo dai set seguenti: da 0 a 9, da A a Z, da a a z e tutti gli altri segni di punteggiatura tranne il punto esclamativo ( ), la virgola (,), la parentesi di apertura ( ) e la parentesi di chiusura ( ), ovvero i caratteri ASCII 0x20, 0x22 fino a 0x2d, 0x2f fino \! \[ a \] 0x5a, 0x5c, 0x5d fino 0x7f.

<!-- end list -->

  - Non può iniziare con uno spazio.

<!-- end list -->

  - Deve contenere almeno un carattere non spazio.

**coltyp**

Tipo della colonna, ad esempio testo, binario o numerico. Per altre informazioni, [vedere](./jet-coltyp.md)JET_COLTYP .

**cbMax**

Lunghezza massima, in byte, di una colonna a lunghezza variabile. Lunghezza della colonna per le colonne a lunghezza fissa.

**grbit**

Gruppo di bit che contengono le opzioni per questa struttura e che includono zero o più dei valori seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La colonna è fissa. Userà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna. JET_bitColumnFixed non può essere usato con JET_bitColumnTagged. Questo bit non può essere usato con valori lunghi, ad esempio <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>La colonna è contrassegnata con tag. Le colonne contrassegnate non accettano spazio nel database se non contengono dati. Questo bit non può essere usato con JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La colonna non deve mai essere impostata su un valore NULL.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La colonna viene incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. Il numero, tuttavia, potrebbe non essere continuo. Ad esempio, se in una tabella vengono inserite cinque righe, la colonna dell'incenerimento automatico potrebbe contenere i valori { 1, 2, 6, 7, 8 }.</p><p><strong>Windows 2000:</strong> Questo bit può essere usato solo in colonne di <strong>tipo JET_coltypLong</strong>.</p><p><strong>Windows Server 2003 e versioni successive:</strong> Questo bit può essere usato solo in colonne di <strong>tipo JET_coltypLong</strong> <strong>o JET_coltypCurrency</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Questo bit è valido solo per le chiamate <a href="gg269215(v=exchg.10).md">a JetGetColumnInfo.</a></p> | 
| <p>JET_bitColumnTTKey</p> | <p>Questo bit è valido solo per le chiamate <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Questo bit è valido solo per le chiamate <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La colonna può essere multivalore. A una colonna multivalore possono essere associati zero, uno o più valori. I vari valori in una colonna multivalore sono identificati dal membro <strong>itagSequence</strong> di varie strutture, ad esempio <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Le colonne multivalore devono essere colonne con tag. non possono essere colonne a lunghezza fissa o a lunghezza variabile.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>La colonna è una colonna di aggiornamento del deposito. Una colonna di aggiornamento del deposito può essere aggiornata contemporaneamente da sessioni diverse con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e mantenere la coerenza transazionale.</p><ul><li><p>È possibile creare una colonna di aggiornamento del deposito solo quando la tabella è vuota.</p></li><li><p>Una colonna di aggiornamento del deposito deve essere di <strong>tipo JET_coltypLong.</strong></p></li><li><p>Una colonna di aggiornamento del deposito deve avere un valore predefinito , ovvero <strong>cbDefault</strong> deve essere positivo.</p></li><li><p>JET_bitColumnEscrowUpdate può essere usato in combinazione con le costanti seguenti:</p><ul><li><p>JET_bitColumnTagged</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li></ul></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La colonna viene creata senza una versione. Le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. Questo bit è utile solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Non può essere usato all'interno di una transazione.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Riservato per utilizzi futuri.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Usare JET_bitColumnDeleteOnZero invece di JET_bitColumnFinalize. JET_bitColumnFinalize specifica che una colonna può essere finalizzata. Quando una colonna che può essere finalizzata ha una colonna di aggiornamento del deposito che raggiunge zero, la riga verrà eliminata. Le versioni future possono invece richiamare una funzione di callback. Per altre informazioni, <a href="gg294098(v=exchg.10).md">vedere</a>JET_CALLBACK . Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito. JET_bitColumnFinalize non può essere usato con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Il valore predefinito per una colonna viene fornito dalla funzione di callback, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. <strong>pvDefault</strong> deve puntare a una <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p><p>JET_bitColumnUserDefinedDefault non può essere usato in combinazione con le costanti seguenti:</p><ul><li><p>JET_bitColumnFixed</p></li><li><p>JET_bitColumnNotNULL</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li><li><p>JET_bitColumnUpdatable</p></li><li><p>JET_bitColumnEscrowUpdate</p></li><li><p>JET_bitColumnFinalize</p></li><li><p>JET_bitColumnDeleteOnZero</p></li><li><p>JET_bitColumnMaybeNull</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato. Un uso comune per una colonna che può essere finalizzata è quello di usarla come campo di conteggio dei riferimenti e quando il campo raggiunge zero il record viene eliminato. JET_bitColumnDeleteOnZero è correlato alla JET_bitColumnFinalize. Una colonna delete-on-zero deve essere una colonna di aggiornamento del deposito. JET_bitColumnDeleteOnZero non può essere usato con JET_bitColumnFinalize. JET_bitColumnDeleteOnZero non può essere usato con colonne predefinite definite dall'utente.</p> | 



**pvDefault**

Punta a un buffer che sarà il valore predefinito per una colonna. La lunghezza del buffer è **cbDefault.** Se non è presente alcun valore predefinito, **pvDefault** deve essere impostato su NULL e **cbDefault** deve essere impostato su zero. Se *grbit* ha JET_bitColumnUserDefinedDefault impostato, **pvDefault** verrà interpretato come un puntatore a una JET_USERDEFINEDDEFAULT struttura . I valori predefiniti non possono essere maggiori di 255 byte. Se un valore predefinito è maggiore di 255 byte, verrà troncato automaticamente.

**cbDefault**

Dimensione, in byte, del buffer specificato da **pvDefault.**

**cp**

Tabella codici per la colonna. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore zero indica che verrà usato il valore predefinito (inglese, 1252). Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.

**columnid**

In caso di esito positivo, l'identificatore di colonna della colonna appena creata verrà passato nuovamente in questo campo. In caso di errore, il valore non è definito.

**Err**

Il **campo err** conterrà lo stato di creazione di questa colonna. Per un elenco dei valori restituiti probabili, vedere [JetAddColumn.](./jetaddcolumn-function.md)

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_COLUMNCREATE_W</strong> (Unicode) <strong>e JET_COLUMNCREATE_A</strong> (ANSI).</p> | 



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
[Oggetti JetSetColumns](./jetsetcolumns-function.md)
