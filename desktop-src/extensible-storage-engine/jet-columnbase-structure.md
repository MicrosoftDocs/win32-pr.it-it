---
description: 'Altre informazioni su: JET_COLUMNBASE Structure'
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
ms.openlocfilehash: eb9ac3377e97079794a8d4c81d4f8be59587870c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468648"
---
# <a name="jet_columnbase-structure"></a>Struttura JET_COLUMNBASE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_columnbase-structure"></a>Struttura JET_COLUMNBASE

La **JET_COLUMNBASE** struttura descrive i parametri di una colonna di base. Le [funzioni JetGetColumnInfo](./jetgetcolumninfo-function.md) [e JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) usano la **JET_COLUMNBASE** struttura .

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

Dimensioni di questa struttura, in byte. Impostare **cbStruct** su sizeof( JET_COLUMNBASE ).

**columnid**

Riservato. Impostare **columnid** su 0 (zero).

**coltyp**

Tipo della colonna, ad esempio testo, binario o numerico. Per altre informazioni, [vedere](./jet-coltyp.md)JET_COLTYP .

**wCountry**

Riservato. Impostare su 0 (zero).

**langid**

Riservato. Impostare su 0 (zero).

**cp**

Tabella codici per la colonna. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore zero indica che verrà usato il valore predefinito (inglese, 1252). Se la colonna non è una colonna di testo, la tabella codici viene impostata automaticamente su zero.

**wFiller**

Riservato. Impostare su 0 (zero).

**cbMax**

Lunghezza massima, in byte, di una colonna a lunghezza variabile o lunghezza effettiva, in byte, di una colonna a lunghezza fissa.

**grbit**

Opzioni per la colonna, inclusi zero o più dei valori seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La colonna è fissa e occupa la stessa quantità di spazio in una riga indipendentemente dalla quantità di dati in essa contenuti. JET_bitColumnFixed può essere combinato con JET_bitColumnTagged e non può essere usato quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLongText</strong> <strong>o JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>La colonna viene contrassegnata e occupa spazio nel database solo se contiene dati. JET_bitColumnTagged può essere combinato con JET_bitColumnFixed, JET_bitColumnVersion o JET_bitColumnEscrowUpdate.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La colonna non deve essere impostata su un <strong>valore NULL.</strong></p><p>JET_bitColumnNotNULL può essere combinato con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnVersion</p> | <p>La colonna è una colonna versione che specifica la versione della riga. Il valore di questa colonna inizia da zero e viene incrementato automaticamente per ogni aggiornamento della riga.</p><p>JET_bitColumnVersion può essere usato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong> e non può essere combinato con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged o JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La colonna viene incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. I numeri, tuttavia, potrebbero non essere sequenziali. Ad esempio, se in una tabella vengono inserite cinque righe, la colonna incrementata automaticamente potrebbe contenere i valori { 1, 2, 6, 7, 8 }.</p><p>JET_bitColumnAutoincrement può essere usato solo quando il membro <strong>coltyp</strong> è impostato su <strong>JET_coltypLong</strong> o JET_coltypCurrency e non può essere combinato con JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault o <strong>JET_bitColumnVersion.</strong></p><p><strong>Windows 2000:</strong> JET_bitColumnVersion può essere usato solo quando il <strong>membro coltyp</strong> è impostato su <strong>JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Valido solo per le chiamate <a href="gg269215(v=exchg.10).md">a JetGetColumnInfo.</a> JET_bitColumnUpdatable non può essere combinato con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Valido solo per le chiamate <a href="gg294118(v=exchg.10).md">a JetOpenTable.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Valido solo per le chiamate <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La colonna può essere multivalore. A una colonna multivalore possono essere associati zero, uno o più valori. I vari valori in una colonna multivalore sono identificati da un numero nel membro <strong>itagSequence</strong> di varie strutture, ad esempio <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Le colonne multivalore devono essere colonne con tag. in altre informazioni, potrebbero non essere colonne a lunghezza fissa o a lunghezza variabile.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Specifica che una colonna è una colonna di aggiornamento del deposito che può essere aggiornata contemporaneamente da sessioni diverse con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e avrà coerenza transazionale.</p><ul><li><p>È possibile creare una colonna di aggiornamento del deposito solo quando la tabella è vuota.</p></li></ul><ul><li><p>Per una colonna di aggiornamento del deposito, il <strong>membro coltyp</strong> deve essere impostato su <strong>JET_coltypLong.</strong></p></li></ul><ul><li><p>Una colonna di aggiornamento del deposito deve avere un valore predefinito , ovvero <strong>cbDefault</strong> deve essere positivo.</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate può essere combinato con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La colonna viene creata senza un numero di versione. Ciò significa che le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. JET_bitColumnUnversioned viene usato solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Non può essere usato all'interno di una transazione.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Riservato per utilizzi futuri.</p><p>JET_bitColumnMaybeNull non può essere combinato con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Non usare. Usare JET_bitColumnDeleteOnZero invece.</p><p>La colonna può essere finalizzata. Una colonna che può essere finalizzata è una colonna di aggiornamento del deposito che determina l'eliminazione della riga quando la colonna raggiunge lo zero. Le versioni future possono richiamare invece una funzione di callback (vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito. JET_bitColumnFinalize può essere combinato con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Il valore predefinito per una colonna verrà fornito da una funzione di callback. Vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. Se JET_bitColumnUserDefinedDefault specificato, <strong>pvDefault</strong> deve puntare a una struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve essere impostato su sizeof( JET_USERDEFINEDDEFAULT ).</p><p>JET_bitColumnUserDefinedDefault può essere combinato con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La colonna è una colonna di aggiornamento del deposito e quando raggiunge lo zero, il record verrà eliminato. Un uso comune per le colonne delete-on-zero è come campi di conteggio dei riferimenti. Quando il numero di riferimenti è pari a zero, il record viene eliminato. Una colonna delete-on-zero deve essere una colonna di aggiornamento del deposito.</p><p>JET_bitColumnDeleteOnZero sostituisce JET_bitColumnFinalize.</p><p>JET_bitColumnDeleteOnZero non può essere combinato con JET_bitColumnFinalize o JET_bitColumnUserDefinedDefault e non può essere usato con colonne predefinite definite dall'utente.</p> | 



**szBaseTableName**

Tabella da cui la tabella corrente eredita il relativo linguaggio DDL.

**szBaseColumnName**

Nome della colonna nella tabella modello.

### <a name="remarks"></a>Commenti

**JET_COLUMNBASE** contiene molte delle stesse informazioni di [JET_COLUMNDEF](./jet-columndef-structure.md), ma aggiunge campi stringa per descrivere la tabella di base (se è stato usato un DDL gerarchico).

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_COLUMNBASE_W</strong> (Unicode) <strong>e JET_COLUMNBASE_A</strong> (ANSI).</p> | 



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
