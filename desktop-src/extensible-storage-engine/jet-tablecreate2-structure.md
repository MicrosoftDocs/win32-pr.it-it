---
description: 'Altre informazioni su: JET_TABLECREATE2 Structure'
title: Struttura JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: 95e4d60ba80317624004fa7c9335005aa16a9300
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476467"
---
# <a name="jet_tablecreate2-structure"></a>Struttura JET_TABLECREATE2


_**Si applica a:** Windows | Windows Server_

## <a name="jet_tablecreate2-structure"></a>Struttura JET_TABLECREATE2

La **JET_TABLECREATE2** contiene le informazioni necessarie per creare una tabella popolata con colonne e indici in un database ESE e che definisce una funzione di callback. La **JET_TABLECREATE2** viene usata da [JetCreateTableColumnIndex2.](./jetcreatetablecolumnindex2-function.md)

**Windows XP:** La **JET_TABLECREATE2** è stata introdotta in Windows XP.

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni di questa struttura in byte (per l'espansione futura). Deve essere impostato su sizeof( JET_TABLECREATE2 ) in byte.

**szTableName**

Nome della tabella da creare.

Il nome deve soddisfare le condizioni seguenti:

  - Avere un valore minore di JET_cbNameMost, senza includere il valore NULL di terminazione.

<!-- end list -->

  - Sono costituiti dal set di caratteri seguente: da 0 a 9, da A a Z, da a a z e da tutti gli altri segni di punteggiatura ad eccezione del punto esclamativo ( ), della virgola (,), della parentesi di apertura ( ) e della parentesi di chiusura ( ), ovvero i caratteri ASCII 0x20, 0x22 fino a 0x2d, 0x2f da 0x5a, 0x5c e 0x5d attraverso \! \[ \] 0x7f.

<!-- end list -->

  - Non iniziare con uno spazio.

<!-- end list -->

  - È costituito da almeno un carattere non spazio.

**szTemplateTableName**

Nome di una tabella già esistente da cui ereditare il linguaggio DDL di base (Data Definition Language). L'uso di una tabella modello consente di creare facilmente molte tabelle con colonne e indici identici.

**ulPages**

Numero iniziale di pagine di database da allocare per la tabella. Se si specifica un numero maggiore di uno, è possibile ridurre la frammentazione se in questa tabella vengono inserite molte righe.

**ulDensity**

Densità della tabella, in punti percentuali. Il numero deve essere 0 o compreso nell'intervallo compreso tra 20 e 100. Il passaggio di 0 indica che deve essere usato il valore predefinito. Il valore predefinito è 80.

**rgcolumncreate**

Matrice di [JET_COLUMNCREATE,](./jet-columncreate-structure.md) ognuna delle quali corrisponde a una colonna da creare nella nuova tabella.

**cColumns**

numero di elementi [JET_COLUMNCREATE](./jet-columncreate-structure.md) in **rgcolumncreate**.

**rgindexcreate**

Matrice di [JET_INDEXCREATE,](./jet-indexcreate-structure.md) ognuna delle quali corrisponde a un indice da creare nella nuova tabella.

**cIndexes**

Numero di elementi [JET_INDEXCREATE](./jet-indexcreate-structure.md) in **rgindexcreate**.

**szCallback**

Funzione che viene chiamata durante determinati eventi. **cbtyp determina** quando verrà chiamata la funzione di callback.

Il formato **di szCallback** deve essere "module function", ad esempio "alpha beta" fa riferimento alla funzione beta nel modulo \! denominato \! "alpha". Il prototipo della funzione deve [corrispondere](./jet-callback-callback-function.md)JET_CALLBACK . Per altre informazioni, [vedere](./jet-callback-callback-function.md)JET_CALLBACK .

**cbtyp**

Descrive il tipo di funzione di callback designata da **szCallback**. Per altre informazioni, [vedere](./jet-cbtyp.md)JET_CBTYP . Questo campo di bit è costituito da uno o più dei bit seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>La funzione di callback verrà chiamata quando una colonna che può essere finalizzata è passata a zero.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>La funzione di callback verrà chiamata prima dell'inserimento del record.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>La funzione di callback verrà chiamata al termine dell'inserimento di un record da parte del motore di database.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>La funzione di callback verrà chiamata prima della modifica di un record.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>La funzione di callback verrà chiamata dopo il completamento della modifica di un record.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>La funzione di callback verrà chiamata prima dell'eliminazione di un record.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>La funzione di callback verrà chiamata dopo l'eliminazione di un record.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>La funzione di callback verrà chiamata per calcolare un valore predefinito definito dall'utente.</p> | 
| <p>JET_cbtypOnlineDefragCompleted</p> | <p>La funzione di callback verrà chiamata dopo il completamento di una chiamata a <a href="gg294095(v=exchg.10).md">JetDefragment2.</a></p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>La funzione di callback verrà chiamata quando deve essere liberata l'archiviazione locale associata a un cursore.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>La funzione di callback verrà chiamata quando deve essere liberata l'archiviazione locale associata a una tabella.</p> | 



**grbit**

Gruppo di bit che contengono le opzioni per questa chiamata, che includono zero o più dei valori seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>L'JET_bitTableCreateFixedDDL impedisce le operazioni DDL sulla tabella, ad esempio l'aggiunta o la rimozione di colonne.</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>L JET_bitTableCreateTemplateTable imposta la tabella come tabella modello. Le nuove tabelle possono quindi specificare il nome di questa tabella come tabella modello. L'impostazione JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Deve essere usato in combinazione con JET_bitTableCreateTemplateTable. Deprecato. Non usare.</p> | 



**tableid**

Campo di output che contiene il [JET_TABLEID](./jet-tableid.md) della nuova tabella se la chiamata API ha esito positivo. Se la chiamata API ha esito negativo, il valore non è definito.

**cCreated**

Campo di output che contiene il numero di oggetti creati se la chiamata API ha esito positivo. Se la chiamata API ha esito negativo, il valore non è definito.

Il numero di oggetti creati è uguale alla somma di colonne, tabelle e indici creati correttamente.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_TABLECREATE2_W</strong> (Unicode) <strong>e JET_TABLECREATE2_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
