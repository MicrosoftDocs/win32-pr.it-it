---
description: 'Altre informazioni su: struttura JET_SPACEHINTS'
title: Struttura JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
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
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305759"
---
# <a name="jet_spacehints-structure"></a>Struttura JET_SPACEHINTS


_**Si applica a:** Windows | Windows Server_

## <a name="jet_spacehints-structure"></a>Struttura JET_SPACEHINTS

La struttura di **JET_SPACEHINTS** contiene informazioni sui modelli di allocazione dello spazio quando un albero b aumenta attraverso le divisioni di accodamento o Hotpoint. Le divisioni di Accodamento si verificano quando vengono aggiunti record alla fine di un albero b e si verificano divisioni Hotpoint quando più record vengono aggiunti allo stesso punto di inserimento virtuale (ad esempio, aggiungendo ' Marie ',' Mark ',' Martin '',' Mary ' al centro di una struttura b-tree ordinata in ordine alfabetico).

**Windows 7:** La struttura **JET_SPACEHINTS** è stata introdotta in Windows 7.

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensione, in byte, della struttura. Impostare questo membro su sizeof (JET_SPACEHINTS).

**ulInitialDensity**

Densità in corrispondenza del layout (Accodamento).

**cbInitial**

Dimensioni iniziali (in byte) dell'oggetto da creare. Deve essere un multiplo delle dimensioni della pagina del database.

**grbit**

Gruppo di bit che contiene le opzioni da utilizzare per questa struttura, che includono zero o più degli elementi seguenti.

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
<td><p>JET_bitSpaceHintsUtilizeParentSpace<br />
0x00000001</p></td>
<td><p>Modifica i criteri di allocazione interna per ottenere spazio heirarchically dall'elemento padre diretto di un albero b.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateHintAppendSequential<br />
0x00000002</p></td>
<td><p>Consente di aumentare il comportamento di suddivisione dell'accodamento in base alla dinamica di crescita della tabella (impostata da cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCreateHintHotpointSequential<br />
0x00000004</p></td>
<td><p>Consente di aumentare il comportamento di suddivisione Hotpoint in base alla dinamica di crescita della tabella (impostata da cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveHintTableScanForward<br />
0x00000010</p></td>
<td><p>Se impostato, il client indica che l'analisi sequenziale di avanzamento è il modello di utilizzo predominante della tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveHintTableScanBackward<br />
0x00000020</p></td>
<td><p>Se impostato, il client indica che l'analisi sequenziale indietro è il modello di utilizzo predominante della tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDeleteHintTableSequential<br />
0x00000100</p></td>
<td><p>Se impostato, l'applicazione prevede che la tabella venga pulita in ordine sequenziale, dalla chiave più bassa alla chiave più alta.</p></td>
</tr>
</tbody>
</table>


**ulMaintDensity**

densità per mulMaintDensity

Densità da gestire all'indirizzo. Se gli hint di spazio specificano JET_bitRetrieveHintTableScanForward o JET_bitRetrieveHintTableScanBackward, la deframmentazione della tabella verrà attivata quando lo spazio utilizzato nella tabella scende al di sotto di questa soglia. La deframmentazione della tabella può essere disabilitata impostando questo membro su zero. Se si imposta questo membro su 100, la deframmentazione della tabella verrà eseguita non appena viene liberata una pagina.

**ulGrowth**

Percentuale di incremento rispetto all'ultimo aumento o alla dimensione iniziale, arrotondata alle dimensioni di allocazione del JET nativo più vicine.

**cbMinExtent troppo piccola**

Viene eseguito l'override di ulGrowth se è troppo piccolo.

**cbMaxExtent**

Valore massimo per la crescita in byte. Questo ulGrowth Caps.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Quando un albero b aumenta attraverso le divisioni di accodamento o Hotpoint (in contrapposizione agli inserimenti di record casuali), la quantità di spazio che la tabella aumenterà è calcolata come segue:

1.  Al momento della creazione, viene fornito il cbInitial dell'albero b, sempre.

2.  Durante la prima allocazione di una determinata area, si essegnerà: cbInitial \* ulGrowth/100 (arrotondato alle dimensioni di pagina del database) o cbMinExtent se più grande.

3.  Durante l'allocazione successiva, cbLastAlloc \* ulGrowth/100 (arrotondato alle dimensioni di pagina del database) o cbMinExtent se più grande.

4.  A una certa allocazione (che potrebbe essere la prima allocazione), le dimensioni calcolate supereranno cbMaxExtent e la dimensione di crescita sarà successiva.

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
