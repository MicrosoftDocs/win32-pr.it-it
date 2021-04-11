---
description: 'Altre informazioni su: funzione JetGetTableColumnInfo'
title: JetGetTableColumnInfo (funzione)
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104235243"
---
# <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo (funzione)

La funzione **JetGetTableColumnInfo** recupera le informazioni su una colonna della tabella.

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*TableID*

Tabella contenente la colonna per la quale recuperare le informazioni.

*szColumnName*

Nome della colonna per cui recuperare le informazioni.

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo di buffer dipende da *InfoLevel*. Il chiamante deve essere configurato per allineare il buffer in modo appropriato.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult*.

*InfoLevel*

Tipo di informazioni che verranno recuperate per la colonna specificata da *szColumnName*. Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*. Per lo schema della tabella temporanea, vedere [JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid Ordina la tabella temporanea *ColumnID*.

  - JET_ColInfoListCompact comprimerà l'output. Per ulteriori informazioni sull'output di Compact, vedere [JET_COLUMNLIST](./jet-columnlist-structure.md).

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
<td><p>JET_ColInfo</p></td>
<td><p><em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e i campi della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> sono compilati in modo appropriato. JET_ColInfo e JET_ColInfoByColid recuperano le stesse informazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Questa operazione è simile a una struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati. Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p><em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, ad eccezione del fatto che questo <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo e JET_ColInfoByColid recuperano le stesse informazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati. Viene aperta una tabella temporanea che viene identificata dal membro <em>TableID</em> del <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. La tabella deve essere chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati. Viene aperta una tabella temporanea che viene identificata dal membro <em>TableID</em> del <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. La tabella deve essere chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>Come JET_ColInfoList, tuttavia, la tabella risultante viene ordinata in base a <em>ColumnID</em>, anziché al nome della colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor è deprecato e l'uso di esso restituirà JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>Come JET_ColInfoBase, <em>pvResult</em> viene interpretato come <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, ad eccezione del fatto che questo <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p>
<p><strong>Windows Vista:  </strong> Questa operazione è disponibile in Windows Vista e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Restituire solo colonne non derivate (se la tabella è derivata da un modello).</p>
<p>Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Restituisce solo il nome della colonna e il ColumnID di ogni colonna.</p>
<p>Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Ordina elenco colonne restituite in base a ColumnID (l'impostazione predefinita consiste nell'ordinare l'elenco in base al nome della colonna).</p>
<p>Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</p></td>
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
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonna denominata <em>szColumnName</em> non è stata trovata nella tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>È stato specificato un <em>InfoLevel</em> non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Questo errore può essere restituito se:</p>
<ul>
<li><p>È stato specificato un nome non valido per <em>szTableName</em> .</p></li>
<li><p>È stato specificato un nome non valido per <em>szColumnName</em> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Questo errore può essere restituito se:</p>
<ul>
<li><p>È stato specificato un <em>InfoLevel</em> non valido.</p></li>
<li><p>È stato passato un <em>SZTABLENAME</em> null.</p></li>
<li><p>Il buffer è troppo piccolo.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

**JetGetTableColumnInfo** e [JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperano entrambe le informazioni relative a una colonna. La differenza tra di esse è la modalità di identificazione della tabella:

  - **JetGetTableColumnInfo** identifica una tabella in base a *TableID*.

  - [JetGetColumnInfo](./jetgetcolumninfo-function.md) identifica una tabella in base alla combinazione *dbid* e *szTableName* .

Quando si recuperano dati con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, viene aperta una tabella temporanea. La tabella temporanea contiene dati e la struttura [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene informazioni sufficienti per attraversare la tabella temporanea. La tabella temporanea deve essere chiusa con [JetCloseTable](./jetclosetable-function.md).

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
<td><p>Implementato come <strong>JetGetTableColumnInfoW</strong> (Unicode) e <strong>JetGetTableColumnInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[Errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md)  
[Parametri di gestione degli errori](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo]()
