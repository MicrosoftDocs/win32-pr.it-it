---
description: 'Altre informazioni su: funzione JetGetTableInfo'
title: Funzione JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968432"
---
# <a name="jetgettableinfo-function"></a>Funzione JetGetTableInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgettableinfo-function"></a>Funzione JetGetTableInfo

La funzione **JetGetTableInfo** Recupera varie informazioni su una tabella in un database.

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Tabella a cui si applicano le informazioni.

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo di buffer dipende da *InfoLevel*. È responsabilità del chiamante allineare il buffer in modo appropriato.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult*.

*InfoLevel*

Tipo di informazioni che verranno recuperate per la tabella specificata da *TableID*. Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*.

Per questo parametro è possibile impostare le opzioni seguenti:

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
<td><p>JET_TblInfo</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> . Se il metodo ha esito positivo, la struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> viene compilata con i dati appropriati. Se ha esito negativo, il contenuto non è definito.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoDbid</p></td>
<td><p><em>pvResult</em> viene considerato come una matrice di due oggetti <a href="gg269248(v=exchg.10).md">JET_DBID</a> . L'identificatore del database proprietario della tabella viene archiviato due volte in questa matrice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoDumpTable</p></td>
<td><p>JET_TblInfoDumpTable è deprecato. L'API restituirà JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoName</p></td>
<td><p>JET_TblInfoName Recupera il nome della tabella e lo archivia in <em>pvResult</em>. Se il buffer è troppo piccolo, il comportamento non è definito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoMostMany</p></td>
<td><p>JET_TblInfoMostMany Recupera il nome della tabella e lo archivia in <em>pvResult</em>. Se il buffer è troppo piccolo, il comportamento non è definito.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoOLC</p></td>
<td><p>JET_TblInfoOLC è deprecato. L'API restituirà JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoRvt</p></td>
<td><p>JET_TblInfoRvt è deprecato. L'API restituirà JET_errQueryNotSupported.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoResetOLC</p></td>
<td><p>JET_TblInfoResetOLC è deprecato. L'API restituirà JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> viene interpretato come una matrice di due ULONG:</p>
<ul>
<li><p>Il primo <strong>ULONG</strong> è il numero di pagine nella tabella.</p></li>
<li><p>Il secondo <strong>ULONG</strong> è la densità di destinazione delle pagine per la tabella.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceAvailable</p></td>
<td><p><em>pvResult</em> viene interpretato come <strong>ULONG</strong>. <strong>ULONG</strong> è la somma del numero di pagine disponibili nella tabella, dei relativi indici e dell'albero del valore Long.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceOwned</p></td>
<td><p><em>pvResult</em> viene interpretato come <strong>ULONG</strong>. <strong>ULONG</strong> è la somma del numero di pagine di proprietà della tabella, inclusi gli indici e l'albero del valore Long e tutte le pagine disponibili.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceUsage</p></td>
<td><p>Il comportamento dell'API dipende dalla dimensione del buffer passato all'API. I due valori di <em>cbMax</em> devono essere almeno (2 * sizeof (ulong)).</p>
<ul>
<li><p>Se <em>cbMax</em> è (2 * sizeof (ulong)), <em>pvResult</em> viene interpretato come una matrice di due ULONG:</p>
<ul>
<li><p>Il primo <strong>ULONG</strong> è il numero di extent di proprietà della tabella.</p></li>
<li><p>Il secondo <strong>ULONG</strong> è il numero di extent disponibili della tabella.</p></li>
</ul></li>
<li><p><em>pvResult</em> viene interpretato come una matrice di:</p>
<ul>
<li><p>Il primo <strong>ULONG</strong> è il numero di extent di proprietà della tabella.</p></li>
<li><p>Il secondo <strong>ULONG</strong> è il numero di extent disponibili della tabella.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoTemplateTableName</p></td>
<td><p><em>pvResult</em> viene interpretato come un buffer di stringa. Il buffer deve essere almeno JET_cbNameMost + 1, inclusa la terminazione <strong>null</strong>. Se la tabella è una tabella derivata, il buffer verrà compilato con il nome della tabella da cui la tabella derivata eredita la DDL. Se la tabella non è una tabella derivata, il buffer sarà una stringa vuota.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Il buffer è troppo piccolo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>È stato specificato un <em>InfoLevel</em> deprecato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Dimensioni del buffer non corrette.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation</p></td>
<td><p>La tabella passata è una tabella temporanea e non è possibile recuperare il <em>InfoLevel</em> richiesto per una tabella temporanea.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectNotFound</p></td>
<td><p>La tabella passata è una tabella temporanea e non è possibile recuperare il <em>InfoLevel</em> richiesto per una tabella temporanea.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errQueryNotSupported</p></td>
<td><p><em>InfoLevel</em> non è supportato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>La tabella è utilizzata da un'altra operazione di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>La tabella è bloccata da un'altra operazione di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>La tabella viene utilizzata dal sistema. Questo avviso non è irreversibile.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Alcune informazioni non sono valide per le tabelle temporanee (vedere [JetOpenTempTable](./jetopentemptable-function.md)).

Le statistiche della tabella includono il numero di record e il numero di pagine nell'indice cluster, ovvero l'indice contenente i dati del record. È possibile accedere alle statistiche dell'indice separatamente in base al nome, utilizzando [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

#### <a name="requirements"></a>Requisiti

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
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetGetTableInfoW</strong> (Unicode) e <strong>JetGetTableInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)
