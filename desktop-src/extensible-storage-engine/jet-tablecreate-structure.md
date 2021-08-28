---
description: 'Altre informazioni su: JET_TABLECREATE Structure'
title: Struttura JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: fcc6c63b06614eb16379fbb18d59a5459a8e5085
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983034"
---
# <a name="jet_tablecreate-structure"></a>Struttura JET_TABLECREATE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_tablecreate-structure"></a>Struttura JET_TABLECREATE

La **JET_TABLECREATE** contiene le informazioni necessarie per creare una tabella popolata con colonne e indici in un database ESE. La **JET_TABLECREATE** utilizzata da [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni di questa struttura in byte (per l'espansione futura). Deve essere impostato su sizeof( JET_TABLECREATE ) in byte.

**szTableName**

Nome della tabella da creare.

Il nome deve soddisfare le condizioni seguenti:

  - Avere un valore minore di JET_cbNameMost, senza includere il valore NULL di terminazione.

<!-- end list -->

  - Sono costituiti dal set di caratteri seguente: da 0 a 9, da A a Z, da a a z e da tutti gli altri segni di punteggiatura ad eccezione del punto esclamativo ( ), della virgola (,), della parentesi di apertura ( ) e della parentesi di chiusura ( ), ovvero i caratteri ASCII 0x20, da 0x22 a 0x2d, da 0x2f a 0x5a, 0x5c e 0x5d attraverso \! \[ \] 0x7f.

<!-- end list -->

  - Non iniziare con uno spazio.

<!-- end list -->

  - È costituito da almeno un carattere non spazio.

**szTemplateTableName**

Nome di una tabella già esistente da cui ereditare il linguaggio DDL (Data Definition Language) di base. L'uso di una tabella modello consente di creare facilmente molte tabelle con colonne e indici identici.

**ulPages**

Numero iniziale di pagine di database da allocare per la tabella. Se si specifica un numero maggiore di uno, è possibile ridurre la frammentazione se in questa tabella vengono inserite molte righe.

**ulDensity**

Densità della tabella, in punti percentuali. Il numero deve essere 0 o compreso nell'intervallo compreso tra 20 e 100. Il passaggio di 0 indica che deve essere usato il valore predefinito. Il valore predefinito è 80.

**rgcolumncreate**

Matrice di [JET_COLUMNCREATE,](./jet-columncreate-structure.md) ognuna delle quali corrisponde a una colonna da creare nella nuova tabella.

**cColumns**

Numero di elementi [JET_COLUMNCREATE](./jet-columncreate-structure.md) in **rgcolumncreate**.

**rgindexcreate**

Matrice di [JET_INDEXCREATE,](./jet-indexcreate-structure.md) ognuna delle quali corrisponde a un indice da creare nella nuova tabella.

**cIndexes**

Numero di elementi [JET_INDEXCREATE](./jet-indexcreate-structure.md) in **rgindexcreate**.

**grbit**

Gruppo di bit che contengono le opzioni per questa chiamata, che includono zero o più dei valori seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>L'JET_bitTableCreateFixedDDL impedisce le operazioni DDL sulla tabella, ad esempio l'aggiunta o la rimozione di colonne.</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>L JET_bitTableCreateTemplateTable imposta la tabella come tabella modello. Le nuove tabelle possono quindi specificare il nome di questa tabella come tabella modello. L'JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Deprecato. Non usare.</p> | 



**tableid**

Campo di output che contiene il [JET_TABLEID](./jet-tableid.md) della nuova tabella se la chiamata API ha esito positivo. Se la chiamata API ha esito negativo, il valore non è definito.

**cCreated**

Campo di output che contiene il numero di oggetti creati se la chiamata API ha esito positivo. Se la chiamata API ha esito negativo, il valore non è definito.

Il numero di oggetti creati è uguale alla somma di colonne, tabelle e indici creati correttamente.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_TABLECREATE_W</strong> (Unicode) <strong>e JET_TABLECREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
