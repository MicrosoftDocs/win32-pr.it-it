---
description: 'Altre informazioni su: Funzione JetGetColumnInfo'
title: Funzione JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e7f3473f15682196f1557810ce4e1d4df3d09aaa
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983649"
---
# <a name="jetgetcolumninfo-function"></a>Funzione JetGetColumnInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetcolumninfo-function"></a>Funzione JetGetColumnInfo

La **funzione JetGetColumnInfo** recupera informazioni su una colonna.

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*Dbid*

Identifica, insieme a *szTableName,* la tabella che contiene la colonna da cui vengono recuperate le informazioni.

*szTableName*

Identifica, insieme a *dbid*, la tabella che contiene la colonna da cui vengono recuperate le informazioni.

*szColumnName*

Nome della colonna per cui vengono recuperate le informazioni.

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo del buffer dipende da *InfoLevel.* Il chiamante deve essere configurato per allineare il buffer in modo appropriato.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult.*

*InfoLevel*

Tipo di informazioni da recuperare per la colonna specificata da *szColumnName*. Il formato dei dati archiviati in *pvResult* dipende da questo parametro. Per lo schema della tabella temporanea, vedere [JET_COLUMNLIST](./jet-columnlist-structure.md).

Questi *InfoLevel si* differenziano per:

  - JET_ColInfoListSortColumnid la tabella temporanea verrà ordinata in base *a columnid*.

  - JET_ColInfoListCompact compatterà l'output. Per altre informazioni sull'output compatto, [vedere JET_COLUMNLIST](./jet-columnlist-structure.md).

Le opzioni seguenti sono disponibili per l'uso con questo parametro.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p>JET_ColInfo e JET_ColInfoByColid recuperano entrambe le stesse informazioni. <em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">un JET_COLUMNDEF</a>e i campi della struttura JET_COLUMNDEF <a href="gg294130(v=exchg.10).md">vengono</a> compilati in modo appropriato.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> struttura . È simile a una <a href="gg294130(v=exchg.10).md">struttura JET_COLUMNDEF</a> struttura . Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati. Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</p> | 
| <p>JET_ColInfoByColid</p> | <p>Come JET_ColInfo, <em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">un JET_COLUMNDEF ,</a>ad eccezione del fatto che <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> struttura . Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati. Viene aperta una tabella temporanea identificata dal membro <strong>tableid</strong> della <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> struttura . La tabella deve essere chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable.</a> Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</p> | 
| <p>JET_ColInfoListCompact</p> | <p>Uguale a JET_ColInfoList.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>Uguale a JET_ColInfoList; tuttavia la tabella risultante viene ordinata in base a columnid anziché al nome della colonna.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor è deprecato e l'uso di esso restituirà JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Come JET_ColInfoBase, <em>pvResult</em> viene interpretato come <a href="gg269194(v=exchg.10).md">un JET_COLUMNBASE ,</a>ad eccezione del fatto che <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista:</strong> Questo valore è stato introdotto in Windows Vista.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Restituisce solo colonne non derivate (se la tabella è derivata da un modello).</p><p>Questo valore può essere in modo logico o in <em>InfoLevel</em>quando <em>infoLevel di</em> base è JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Questo valore è stato introdotto Windows Vista.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Restituisce solo il nome e l'ID colonna di ogni colonna.</p><p>Questo valore può essere in modo logico o in <em>InfoLevel</em>quando <em>infoLevel di</em> base è JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Questo valore è stato introdotto in Windows Vista.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Ordinare l'elenco delle colonne restituite in base a columnid (l'impostazione predefinita è l'ordinamento dell'elenco in base al nome della colonna).</p><p>Questo valore può essere in modo logico o in <em>InfoLevel</em>quando <em>infoLevel di</em> base è JET_ColInfoList.</p><p><strong>Windows Vista:</strong> Questo valore è stato introdotto in Windows Vista.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonna <em>denominata szColumnName</em> non è stata trovata nella tabella.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>È stato <em>specificato un InfoLevel</em> non valido.</p> | 
| <p>JET_errInvalidName</p> | <p>Questo errore può essere restituito se:</p><ul><li><p>È stato specificato un <em>nome non valido per szTableName.</em></p></li><li><p>È stato specificato un <em>nome non valido per szColumnName.</em></p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Questo errore può essere restituito se:</p><ul><li><p>È stato <em>specificato un InfoLevel</em> non valido.</p></li><li><p>È stato passato un valore NULL <em>szTableName.</em></p></li><li><p>Il buffer è troppo piccolo.</p></li></ul> | 



#### <a name="remarks"></a>Commenti

[JetGetTableColumnInfo e](./jetgettablecolumninfo-function.md) **JetGetColumnInfo** recuperano entrambe le informazioni su una colonna. La differenza tra di essi è il modo in cui viene identificata la tabella:

  - [JetGetTableColumnInfo identifica](./jetgettablecolumninfo-function.md) una tabella in base a *tableid*.

  - **JetGetColumnInfo identifica** una tabella in base alla *combinazione dbid* *e szTableName.*

Quando si recuperano dati con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, verrà aperta una tabella temporanea. La tabella temporanea contiene dati e la [struttura JET_COLUMNLIST](./jet-columnlist-structure.md) contiene informazioni sufficienti per attraversare la tabella temporanea. La tabella temporanea deve essere chiusa con [JetCloseTable.](./jetclosetable-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetColumnInfoW</strong> (Unicode) e <strong>JetGetColumnInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
