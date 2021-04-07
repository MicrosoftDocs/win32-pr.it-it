---
description: 'Altre informazioni su: struttura JET_TABLECREATE2'
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
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885781"
---
# <a name="jet_tablecreate2-structure"></a>Struttura JET_TABLECREATE2


_**Si applica a:** Windows | Windows Server_

## <a name="jet_tablecreate2-structure"></a>Struttura JET_TABLECREATE2

La struttura **JET_TABLECREATE2** contiene le informazioni necessarie per creare una tabella popolata con colonne e indici in un database ESE e che designa una funzione di callback. La struttura **JET_TABLECREATE2** viene utilizzata da [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).

**Windows XP:** La struttura **JET_TABLECREATE2** è stata introdotta in Windows XP.

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

Dimensioni in byte della struttura (per l'espansione futura). Deve essere impostato su sizeof (JET_TABLECREATE2) in byte.

**szTableName**

Nome della tabella da creare.

Il nome deve essere utilizzato per soddisfare le condizioni seguenti:

  - Hanno un valore minore di JET_cbNameMost, escluso il valore NULL di terminazione.

<!-- end list -->

  - Sono costituiti dal set di caratteri seguente: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.

<!-- end list -->

  - Non iniziare con uno spazio.

<!-- end list -->

  - Sono costituiti da almeno un carattere diverso dallo spazio.

**szTemplateTableName**

Nome di una tabella già esistente da cui ereditare DDL di base (Data Definition Language). L'utilizzo di una tabella modello consente la creazione semplificata di molte tabelle con colonne e indici identici.

**ulPages**

Numero iniziale di pagine del database da allocare per la tabella. La specifica di un numero maggiore di uno può ridurre la frammentazione se nella tabella vengono inserite molte righe.

**ulDensity**

Densità della tabella, in punti percentuali. Il numero deve essere 0 o compreso tra 20 e 100. Il valore 0 indica che deve essere utilizzato il valore predefinito. Il valore predefinito è 80.

**rgcolumncreate**

Matrice di strutture di [JET_COLUMNCREATE](./jet-columncreate-structure.md) , ciascuna delle quali corrisponde a una colonna da creare nella nuova tabella.

**cColumns**

numero di elementi [JET_COLUMNCREATE](./jet-columncreate-structure.md) in **rgcolumncreate**.

**rgindexcreate**

Matrice di strutture di [JET_INDEXCREATE](./jet-indexcreate-structure.md) , ciascuna delle quali corrisponde a un indice da creare nella nuova tabella.

**cIndexes**

Numero di elementi [JET_INDEXCREATE](./jet-indexcreate-structure.md) in **rgindexcreate**.

**szCallback**

Funzione che viene chiamata durante alcuni eventi. **cbtyp** determina quando verrà chiamata la funzione di callback.

Il formato di **szCallback** deve essere " \! function module", ad esempio "Alpha \! beta" si riferisce alla funzione beta nel modulo denominato "Alpha". Il prototipo della funzione deve corrispondere [JET_CALLBACK](./jet-callback-callback-function.md). Per ulteriori informazioni, vedere [JET_CALLBACK](./jet-callback-callback-function.md).

**cbtyp**

Descrive il tipo di funzione di callback designato da **szCallback**. Per ulteriori informazioni, vedere [JET_CBTYP](./jet-cbtyp.md). Questo bit è costituito da uno o più dei seguenti bit.

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
<td><p>JET_cbtypFinalize</p></td>
<td><p>La funzione di callback verrà chiamata quando una colonna che può essere finalizzata è scesa a zero.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>La funzione di callback verrà chiamata prima dell'inserimento del record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterInsert</p></td>
<td><p>La funzione di callback verrà chiamata al termine dell'inserimento di un record da parte del motore di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeReplace</p></td>
<td><p>La funzione di callback verrà chiamata prima della modifica di un record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterReplace</p></td>
<td><p>La funzione di callback verrà chiamata dopo il completamento della modifica di un record.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeDelete</p></td>
<td><p>La funzione di callback verrà chiamata prima dell'eliminazione di un record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterDelete</p></td>
<td><p>La funzione di callback verrà chiamata dopo l'eliminazione di un record.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypUserDefinedDefaultValue</p></td>
<td><p>La funzione di callback verrà chiamata per calcolare un valore predefinito definito dall'utente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypOnlineDefragCompleted</p></td>
<td><p>La funzione di callback verrà chiamata dopo il completamento di una chiamata a <a href="gg294095(v=exchg.10).md">JetDefragment2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>La funzione di callback verrà chiamata quando è necessario liberare l'archivio locale associato a un cursore.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>La funzione di callback verrà chiamata quando l'archiviazione locale associata a una tabella deve essere liberata.</p></td>
</tr>
</tbody>
</table>


**grbit**

Gruppo di bit che contiene le opzioni per la chiamata, che includono zero o più dei valori seguenti.

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
<td><p>JET_bitTableCreateFixedDDL</p></td>
<td><p>L'impostazione di JET_bitTableCreateFixedDDL impedisce operazioni DDL nella tabella, ad esempio l'aggiunta o la rimozione di colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Impostando JET_bitTableCreateTemplateTable la tabella è una tabella modello. Le nuove tabelle possono quindi specificare il nome della tabella come tabella del modello. L'impostazione JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Deve essere utilizzato insieme a JET_bitTableCreateTemplateTable. Deprecato. Non usare.</p></td>
</tr>
</tbody>
</table>


**TableID**

Un campo di output che include il [JET_TABLEID](./jet-tableid.md) della nuova tabella se la chiamata API ha esito positivo. Se la chiamata API ha esito negativo, il valore non è definito.

**Creata**

Un campo di output che contiene il numero di oggetti creati se la chiamata API ha esito positivo. Se la chiamata API ha esito negativo, il valore non è definito.

Il numero di oggetti creati è uguale alla somma di colonne, tabelle e indici creati correttamente.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_TABLECREATE2_W</strong> (Unicode) e <strong>JET_TABLECREATE2_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
