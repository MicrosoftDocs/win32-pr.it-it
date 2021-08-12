---
description: 'Altre informazioni su: JET_SPACEHINTS Structure'
title: JET_SPACEHINTS struttura
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
ms.openlocfilehash: f829e78ff54e77011346ae1bfd39f909411cbee12c18d19781f8fe5d62865097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252256"
---
# <a name="jet_spacehints-structure"></a>JET_SPACEHINTS struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_spacehints-structure"></a>JET_SPACEHINTS struttura

La **JET_SPACEHINTS** contiene informazioni sui modelli di allocazione dello spazio quando un albero b si sviluppa tramite divisioni di accodamento o punto di accesso. Le divisioni di accodamento si verificano quando i record vengono aggiunti alla fine di un albero b e le divisioni di punti di accesso si verificano quando più record vengono aggiunti allo stesso punto di inserimento virtuale, ad esempio aggiungendo "Marie", "Mark", "Martin", "Mary" al centro di un albero b ordinato alfabeticamente.

**Windows 7:** La **JET_SPACEHINTS** è stata introdotta in Windows 7.

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

Dimensione, in byte, della struttura. Impostare questo membro su sizeof( JET_SPACEHINTS ).

**ulInitialDensity**

Densità in corrispondenza del layout (append).

**cbInitial**

Dimensione iniziale (in byte) dell'oggetto da creare. Deve essere un multiplo delle dimensioni della pagina del database.

**grbit**

Gruppo di bit che contengono le opzioni da utilizzare per questa struttura, che includono zero o più dei valori seguenti.

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
<td><p>Modifica i criteri di allocazione interni per ottenere spazio in modo eretico dall'elemento padre immediato di un albero b.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateHintAppendSequential<br />
0x00000002</p></td>
<td><p>Consente l'aumento delle dimensioni del comportamento di divisione di accodamento in base alla dinamica di crescita della tabella (impostata da cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCreateHintHotpointSequential<br />
0x00000004</p></td>
<td><p>Consente l'aumento delle dimensioni del comportamento di suddivisione dei punti di accesso a caldo in base alla dinamica di crescita della tabella (impostata da cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveHintTableScanForward<br />
0x00000010</p></td>
<td><p>Se impostato, il client indica che l'analisi sequenziale in avanti è il modello di utilizzo predominante di questa tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveHintTableScanBackward<br />
0x00000020</p></td>
<td><p>Se impostato, il client indica che l'analisi sequenziale all'indietro è il modello di utilizzo prevalente di questa tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDeleteHintTableSequential<br />
0x00000100</p></td>
<td><p>Se impostata, l'applicazione prevede che la tabella sia pulita in ordine sequenziale, dalla chiave più bassa alla chiave più alta.</p></td>
</tr>
</tbody>
</table>


**ulMaintDensity**

densità in mulMaintDensity

Densità da mantenere. Se gli hint per lo spazio JET_bitRetrieveHintTableScanForward o JET_bitRetrieveHintTableScanBackward, la deframmentazione della tabella verrà attivata quando lo spazio usato nella tabella scende al di sotto di questa soglia. La deframmentazione della tabella può essere disabilitata impostando questo membro su zero. Se si imposta questo membro su 100, la deframmentazione della tabella verrà eseguita non appena viene liberata una pagina.

**ulGrowth**

Crescita percentuale rispetto all'ultima crescita o dimensione iniziale, arrotondata alle dimensioni di allocazione JET native più vicine.

**cbMinExtent troppo piccolo**

Esegue l'override di ulGrowth se troppo piccolo.

**cbMaxExtent**

Valore massimo per la crescita in byte. Questo limite è ulGrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Quando un albero b cresce tramite divisioni di accodamento o punto di accesso (anziché inserimenti casuali di record), la quantità di spazio di cui la tabella aumenta viene calcolata come segue:

1.  Al momento della creazione, si assegna sempre l'albero b cbInitial.

2.  Durante la prima allocazione di una determinata area, verranno allocati: cbInitial ulGrowth/100 (arrotondato alle dimensioni di pagina del database) o \* cbMinExtent se maggiore.

3.  Durante l'allocazione successiva, cbLastAlloc ulGrowth/100 (arrotondato alle dimensioni della pagina del database) o \* cbMinExtent se maggiore.

4.  A un'allocazione (che potrebbe essere la prima allocazione), le dimensioni calcolate supereranno cbMaxExtent e che sarà la dimensione di crescita in seguito.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
