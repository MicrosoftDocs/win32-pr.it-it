---
description: 'Altre informazioni su: struttura JET_CONDITIONALCOLUMN'
title: Struttura JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308496"
---
# <a name="jet_conditionalcolumn-structure"></a>Struttura JET_CONDITIONALCOLUMN


_**Si applica a:** Windows | Windows Server_

## <a name="jet_conditionalcolumn-structure"></a>Struttura JET_CONDITIONALCOLUMN

La struttura **JET_CONDITIONALCOLUMN** definisce il modo in cui viene eseguita l'indicizzazione condizionale per un indice specificato. Un indice condizionale contiene una voce di indice solo per le righe che corrispondono alla condizione specificata. Tuttavia, la colonna condizionale non fa parte della chiave dell'indice, ma controlla solo la presenza della voce di indice.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Membri

**cbStruct**

Questo campo deve essere inizializzato su sizeof (JET_CONDITIONALCOLUMN), in byte.

**szColumnName**

Nome della colonna contenente i dati su cui il motore di database sta indicizzando la riga in modo condizionale.

**grbit** Gruppo di bit che fornisce le opzioni per l'indice condizionale. Il passaggio di valori zero o logici **o** ed non è valido per **JET_CONDITIONALCOLUMN**. Il campo di bit deve essere esattamente uno dei seguenti:

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
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p>La colonna specificata dal parametro <em>szColumnName</em> deve essere null per visualizzare in questo indice una voce di indice per una determinata riga.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p>La colonna specificata dal parametro <em>szColumnName</em> non deve essere null per una voce di indice affinché una determinata riga venga visualizzata in questo indice.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Commenti

Un indice condizionale contiene una voce di indice solo per le righe che corrispondono alla condizione specificata. Una colonna, ad esempio, può essere denominata "contrassegnato" e, quando una riga è contrassegnata, la colonna viene impostata su un valore non NULL. Un JET_bitIndexColumnMustBeNonNull Indice condizionale in questa colonna mostrerà tutte le righe contrassegnate e un indice condizionale JET_bitIndexColumnMustBeNull mostrerà le righe non contrassegnate. Questo è anche un modo pratico per eseguire un'eliminazione di flag e un indice di Garbage Collection.

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
<td><p>Implementato come <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) e <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
