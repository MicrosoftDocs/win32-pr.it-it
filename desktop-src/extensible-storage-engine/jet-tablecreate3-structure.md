---
description: 'Altre informazioni su: JET_TABLECREATE3 struttura'
title: Struttura JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64f820b9e9a42099cdb99d8ab8f0756e8fdbb23256917821d05573afd9068017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979241"
---
# <a name="jet_tablecreate3-structure"></a>Struttura JET_TABLECREATE3


_**Si applica a:** Windows | Windows Server_

La **JET_TABLECREATE3** contiene le informazioni necessarie per creare una tabella popolata con colonne e indici in un database ESE (Extensible Archiviazione Engine) e che definisce una funzione di callback. La **JET_TABLECREATE3** viene usata dalla [funzione JetCreateTableColumnIndex3.](./jetcreatetablecolumnindex3-function.md)

La **JET_TABLECREATE3** è stata introdotta nel sistema operativo Windows 7.

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni della struttura in byte (per l'espansione futura). Deve essere impostato su sizeof( JET_TABLECREATE3 ) in byte.

**szTableName**

Nome della tabella da creare.

Il nome deve soddisfare le condizioni seguenti:

  - Deve avere un valore minore di JET_cbNameMost, senza includere il valore Null di terminazione.

  - Deve essere costituito dal set di caratteri seguente: da 0 a 9, da A a Z, da a a z e da tutti gli altri segni di punteggiatura ad eccezione del punto esclamativo ( ), della virgola (,), della parentesi quadra di apertura ( ) e della parentesi di chiusura ( ), ovvero i caratteri ASCII 0x20, 0x22 fino a 0x2d, 0x2f fino a 0x5a, 0x5c e 0x5d fino \! \[ \] 0x7f.

  - Non deve iniziare con uno spazio.

  - Deve essere costituito da almeno un carattere diverso da uno spazio.

**szTemplateTableName**

Nome di una tabella esistente da cui ereditare il linguaggio DDL (Data Definition Language) di base. L'uso di una tabella modello consente di creare facilmente molte tabelle con colonne e indici identici.

**ulPages**

Numero iniziale di pagine di database da allocare per la tabella. Se si specifica un numero maggiore di uno, è possibile ridurre la frammentazione se in questa tabella vengono inserite molte righe.

**ulDensity**

Densità della tabella, in punti percentuali. Il numero deve essere compreso tra 0 o compreso tra 20 e 100. Il passaggio di 0 indica che deve essere usato il valore predefinito. Il valore predefinito è 80.

**rgcolumncreate**

Matrice di [JET_COLUMNCREATE,](./jet-columncreate-structure.md) ognuna delle quali corrisponde a una colonna da creare nella nuova tabella.

**cColumns**

Numero di [JET_COLUMNCREATE](./jet-columncreate-structure.md) nel *parametro rgcolumncreate.*

**rgindexcreate**

Matrice di [JET_INDEXCREATE2,](./jet-indexcreate2-structure.md) ognuna delle quali corrisponde a un indice da creare nella nuova tabella.

**cIndexes**

Numero di [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) nel parametro *rgindexcreate.*

**szCallback**

Funzione che viene chiamata durante determinati eventi. **cbtyp determina** quando verrà chiamata la funzione di callback.

Il formato di **szCallback** deve essere "module function". Ad esempio, "alpha beta" fa riferimento alla funzione beta nel modulo \! \! denominato "alpha".

Il prototipo della funzione deve corrispondere alla [JET_CALLBACK](./jet-callback-callback-function.md) di callback.

**cbtyp**

Descrive il tipo di funzione di callback designata da **szCallback.** Per altre informazioni, vedere [JET_CBTYP](./jet-cbtyp.md).

Questo campo di bit è costituito da uno o più valori di bit elencati nella tabella seguente.

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
<td><p>La funzione di callback verrà chiamata quando una colonna che può essere finalizzata è passata a zero.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>La funzione di callback verrà chiamata prima dell'inserimento di record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterInsert</p></td>
<td><p>La funzione di callback verrà chiamata dopo che il motore di database ha completato l'inserimento di un record.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeReplace</p></td>
<td><p>La funzione di callback verrà chiamata prima della modifica di un record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterReplace</p></td>
<td><p>La funzione di callback verrà chiamata dopo aver completato la modifica di un record.</p></td>
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
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>La funzione di callback verrà chiamata quando è necessario liberare l'archiviazione locale associata a un cursore.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>La funzione di callback verrà chiamata quando è necessario liberare l'archiviazione locale associata a una tabella.</p></td>
</tr>
</tbody>
</table>


**grbit**

Gruppo di bit che contiene zero o più valori dell'opzione di chiamata elencati nella tabella seguente.

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
<td><p>Impedisce operazioni DDL sulla tabella, ad esempio l'aggiunta o la rimozione di colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Fa in modo che la tabella sia una tabella modello. Le nuove tabelle possono quindi specificare il nome della tabella come tabella modello. L'JET_bitTableCreateTemplateTable implica JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Deve essere usato in combinazione con JET_bitTableCreateTemplateTable. Deprecato. Non usare.</p></td>
</tr>
</tbody>
</table>


**pSeqSpacehints**

Puntatore a una [JET_SPACEHINTS](./jet-spacehints-structure.md) per l'indice sequenziale predefinito.

**pSeqSpacehints** è stato introdotto in Windows 7.

**pLVSpacehints**

Puntatore a una [struttura JET_SPACEHINTS](./jet-spacehints-structure.md) per un albero Valore lungo separato.

**pLVSpacehints** è stato introdotto in Windows 7.

**cbSeparateLV**

Dimensione per separare una VL intrinseca dal record primario. Qualsiasi struttura c di valore lungo per un albero LV separato. Per altre informazioni, vedere ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md). Le colonne con valori lunghi inferiori a questo valore possono essere separate se il record diventa troppo grande.

**cbSeparateLV** è stato introdotto in Windows 7.

**tableid**

Campo di output che contiene il [JET_TABLEID](./jet-tableid.md) della nuova tabella se la chiamata API ha esito positivo. Se la chiamata API non riesce, il valore non è definito. Questa tabella viene aperta esclusivamente.

**cCreated**

Campo di output che contiene il conteggio degli oggetti creati se la chiamata API ha esito positivo. Se la chiamata API non riesce, il valore non è definito.

Il conteggio degli oggetti creati è uguale alla somma di colonne, tabelle e indici creati correttamente.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_TABLECREATE3_W</strong> (Unicode) <strong>e JET_TABLECREATE3_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedi anche

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
