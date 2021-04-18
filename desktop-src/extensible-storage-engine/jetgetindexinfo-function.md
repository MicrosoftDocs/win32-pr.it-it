---
description: 'Altre informazioni su: funzione JetGetIndexInfo'
title: Funzione JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315069"
---
# <a name="jetgetindexinfo-function"></a>Funzione JetGetIndexInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetindexinfo-function"></a>Funzione JetGetIndexInfo

La funzione **JetGetIndexInfo** recupera le informazioni su un indice.

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*dbid*

Identificatore del database da usare per la chiamata API.

*szTableName*

Nome della tabella contenente l'indice con le informazioni da recuperare.

*szIndexName*

Nome dell'indice con le informazioni da recuperare.

*pvResult*

Puntatore a un buffer che riceverà le informazioni desiderate. Il buffer deve essere allineato per contenere il tipo richiesto. Il tipo del buffer dipende dal parametro *InfoLevel* .

*cbResult*

Dimensione, in byte, del buffer passato come *pvResult*.

*InfoLevel*

Informazioni che verranno archiviate in *pvResult*. Per questo parametro è possibile usare le opzioni seguenti.

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
<td><p>JET_IdxInfo</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . In seguito all'esito positivo, la struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> riceve informazioni sull'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>pvResult</em> viene interpretato come ulong. In seguito all'esito positivo, ULONG include il conteggio degli indici nella tabella specificata. <em>szIndexName</em> viene ignorato. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>pvResult</em> viene interpretato come <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. In seguito all'esito positivo, la struttura <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> riceve informazioni sull'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid è deprecato. Usare invece JET_IdxInfoLCID e la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>pvResult</em> viene interpretato come un identificatore LCID. In seguito all'esito positivo, l'LCID include l'identificatore delle impostazioni locali dell'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p>
<p><strong>Windows XP:  </strong> JET_IdxInfoLCID è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . In seguito all'esito positivo, la struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> riceve informazioni sull'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC è obsoleto.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC è obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> viene interpretato come ulong. In seguito all'esito positivo, ULONG determinerà l'utilizzo dello spazio dell'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor è obsoleto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>pvResult</em> viene interpretato come UShort. In caso di esito positivo, il USHORT include il valore di <em>cbVarSegMac</em> usato durante la creazione dell'indice. Per una descrizione di <em>cbVarSegMac</em>, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>pvResult</em> viene interpretato come UShort. In caso di esito positivo, il USHORT include il valore di <em>cbKeyMost</em> usato durante la creazione dell'indice. Per una descrizione di <em>cbKeyMost</em>, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p>
<p><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost è stato introdotto in Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCreateIndex</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex è stato introdotto in Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCreateIndex2</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p>
<p><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 è stato introdotto in Windows 7.</p></td>
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
<td><p>JET_errIndexNotFound</p></td>
<td><p>Impossibile trovare l'indice specificato nella tabella specificata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Il buffer passato come <em>pvResult</em> è troppo piccolo. Il contenuto del buffer non è definito.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

**JetGetIndexInfo** e [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperano informazioni identiche su un indice. La differenza consiste nel modo in cui viene specificata la tabella. **JetGetIndexInfo** prevede un database (*dbid*) e il nome di una tabella (*szTableName*), mentre [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) prevede un identificatore di tabella (*TableID*).

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
<td><p>Implementato come <strong>JetGetIndexInfoW</strong> (Unicode) e <strong>JetGetIndexInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
