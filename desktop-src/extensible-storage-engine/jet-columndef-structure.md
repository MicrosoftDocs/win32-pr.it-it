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
ms.openlocfilehash: fccf3b076b71e8923366a95810d1f3009d4fe1c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471137"
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


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La colonna verrà fissata. Userà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna. JET_bitColumnFixed non può essere usato con JET_bitColumnTagged. Questo bit non può essere usato con valori long (ovvero JET_coltypLongText <strong>e</strong> <strong>JET_coltypLongBinary</strong>).</p> | 
| <p>JET_bitColumnTagged</p> | <p>La colonna verrà contrassegnata con tag. Le colonne contrassegnate non accettano spazio nel database se non contengono dati. Questo bit non può essere usato con JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La colonna non deve mai essere impostata su un valore NULL.</p> | 
| <p>JET_bitColumnVersion</p> | <p>La colonna è una colonna versione che specifica la versione della riga. Il valore di questa colonna inizia da zero e verrà incrementato automaticamente per ogni aggiornamento nella riga.</p><p>Questo bit può essere applicato solo <strong>JET_coltypLong</strong> colonne. Questo bit non può essere usato con JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate o JET_bitColumnTagged.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La colonna verrà incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. I numeri, tuttavia, potrebbero non essere continui. Ad esempio, se in una tabella vengono inserite cinque righe, la colonna "autoincrement" potrebbe contenere i valori { 1, 2, 6, 7, 8 }. Questo bit può essere usato solo in colonne di <strong>tipo JET_coltypLong</strong> <strong>o JET_coltypCurrency</strong>.</p><p><strong>Windows 2000:</strong> In Windows 2000 questo bit può essere usato solo in colonne di <strong>tipo JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Questo bit è valido solo per le chiamate <a href="gg269215(v=exchg.10).md">a JetGetColumnInfo.</a></p> | 
| <p>JET_bitColumnTTKey</p> | <p>Questo bit è valido solo per le chiamate <a href="gg294118(v=exchg.10).md">a JetOpenTable.</a></p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Questo bit è valido solo per le chiamate <a href="gg269211(v=exchg.10).md">a JetOpenTempTable.</a></p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La colonna può essere multivalore. A una colonna multivalore possono essere associati zero, uno o più valori. I vari valori in una colonna multivalore sono identificati da un numero denominato <strong>membro itagSequence,</strong> che appartiene a varie strutture, tra <a href="gg294049(v=exchg.10).md">cui: JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>e <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Le colonne multivalore devono essere colonne con tag. non possono essere colonne a lunghezza fissa o a lunghezza variabile.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Specifica che una colonna è una colonna di aggiornamento del deposito. Una colonna di aggiornamento del deposito può essere aggiornata contemporaneamente da sessioni diverse con <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manterrà la coerenza transazionale. Anche una colonna di aggiornamento del deposito deve soddisfare le condizioni seguenti:</p><ul><li><p>È possibile creare una colonna di aggiornamento del deposito solo quando la tabella è vuota.</p></li></ul><ul><li><p>Una colonna di aggiornamento del deposito deve essere di <strong>tipo JET_coltypLong</strong>.</p></li></ul><ul><li><p>Una colonna di aggiornamento del deposito deve avere un valore predefinito , ovvero <strong>cbDefault</strong> deve essere positivo.</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate può essere usato in combinazione con JET_bitColumnTagged, JET_bitColumnVersion o JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La colonna verrà creata in un oggetto senza informazioni sulla versione. Ciò significa che le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. Questo bit è utile solo con <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Non può essere usato all'interno di una transazione.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Riservato per utilizzi futuri.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Usare JET_bitColumnDeleteOnZero invece di JET_bitColumnFinalize. JET_bitColumnFinalize possibile finalizzare una colonna. Quando una colonna che può essere finalizzata ha una colonna di aggiornamento del deposito che raggiunge zero, la riga verrà eliminata. Le versioni future potrebbero richiamare invece una funzione di callback (per altre informazioni, <a href="gg294098(v=exchg.10).md">vedere JET_CALLBACK</a>). Una colonna che può essere finalizzata deve essere una colonna di aggiornamento del deposito. JET_bitColumnFinalize non può essere usato con JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Il valore predefinito per una colonna verrà fornito da una funzione di callback. Vedere <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. Specificando JET_bitColumnUserDefinedDefault, <strong>pvDefault</strong> deve puntare <a href="gg269200(v=exchg.10).md">a</a> una struttura JET_USERDEFINEDDEFAULT e <strong>cbDefault</strong> deve essere impostato su sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p><ul><li><p>JET_bitColumnUserDefinedDefault non può essere usato in combinazione con JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero o JET_bitColumnMaybeNull.</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La colonna è una colonna di aggiornamento del deposito e, quando raggiunge lo zero, il record verrà eliminato. Un uso comune per una colonna che può essere finalizzata è quello di usarla come campo di conteggio dei riferimenti e quando il campo raggiunge lo zero, il record viene eliminato. JET_bitColumnDeleteOnZero è correlato a JET_bitColumnFinalize. Una colonna Elimina su zero deve essere una colonna di aggiornamento del deposito. JET_bitColumnDeleteOnZero non può essere usato con JET_bitColumnFinalize. JET_bitColumnDeleteOnZero non può essere usato con colonne predefinite definite dall'utente.</p> | 



### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



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
