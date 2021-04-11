---
description: 'Altre informazioni su: funzione JetGetDatabaseInfo'
title: Funzione JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231800"
---
# <a name="jetgetdatabaseinfo-function"></a>Funzione JetGetDatabaseInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetdatabaseinfo-function"></a>Funzione JetGetDatabaseInfo

La funzione **JetGetDatabaseInfo** recupera vari tipi di informazioni sul database. Questa API può essere chiamata quando un database è collegato o in linea (con **JetGetDatabaseInfo**) o mentre il database o il motore di database è offline (con [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*dbid*

[JET_DBID](./jet-dbid.md) per il database da cui recuperare le informazioni.

*pvResult*

Puntatore a un buffer che riceverà le informazioni specificate. La dimensione del buffer, in byte, viene passata in *cbMax*.

In caso di errore, il contenuto di *pvResult* non è definito.

Le informazioni archiviate in *pvResult* dipendono da *InfoLevel*.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult*.

*InfoLevel*

*InfoLevel* specifica il tipo di informazioni da recuperare sul database specificato. Influiscono sul modo in cui *pvResult* viene interpretato. Alcuni *InfoLevel* sono disponibili solo nella versione offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) o in linea (**JetGetDatabaseInfo**) dell'API.

Se il buffer *pvResult* fornito è troppo piccolo, viene restituito JET_errInvalidBufferSize o JET_errBufferTooSmall a seconda del valore di *InfoLevel*.

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
<td><p>JET_DbInfoCollate</p></td>
<td><p>Non ancora supportato e restituisce i valori predefiniti. Non usare.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Questi <em>InfoLevels</em> sono deprecati e non sono attualmente supportati. Non usare.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Non ancora supportato e restituisce i valori predefiniti. Non usare.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Non ancora supportato e restituisce i valori predefiniti. Non usare.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFilename</p></td>
<td><p><em>pvResult</em> verrà interpretato come un buffer di stringa (Char *). È stato suggerito un buffer di MAX_PATH, tuttavia non è obbligatorio. Se la lunghezza del buffer non è sufficiente, verrà restituito JET_errBufferTooSmall. La stringa verrà popolata con il percorso del database per questo DBID.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> verrà interpretato come un valore DWORD (4 byte). Restituisce le dimensioni del database in pagine.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Questi <em>InfoLevels</em> sono deprecati e non sono attualmente supportati. Non usare.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoLCID</p></td>
<td><p>(Windows XP e versioni successive) Questo <em>InfoLevel</em> è stato originariamente specificato come: JET_DbInfoLangid (Windows 2000)</p>
<p><em>pvResult</em> verrà interpretato come Long. Viene restituito l'identificatore delle impostazioni locali (LCID) associato al database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> verrà interpretato come <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La struttura di <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> verrà popolata con le informazioni relative al database specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoOptions</p></td>
<td><p><em>pvResult</em> verrà interpretato come un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Viene restituito un valore che indica se il database è aperto in modalità esclusiva. Se il database è in modalità esclusiva JET_bitDbExclusive verrà impostato nell' <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> fornito; in caso contrario, viene impostato zero. Si noti che non vengono restituite altre opzioni di <em>grbit</em> del database per <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> e <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p>Disponibile solo in Windows XP e versioni successive. <em>pvResult</em> verrà interpretato come unsigned long. Questa operazione restituirà le dimensioni di pagina del database in byte.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoSpaceAvailable</p></td>
<td><p><em>pvResult</em> verrà interpretato come un valore DWORD. Viene restituito lo spazio disponibile per il database in pagine.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoSpaceOwned</p></td>
<td><p><em>pvResult</em> verrà interpretato come un valore DWORD. Viene restituito lo spazio di proprietà del database in pagine.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoTransactions</p></td>
<td><p><em>pvResult</em> verrà interpretato come Long. Verrà restituito un valore maggiore del livello massimo a cui è possibile annidare le transazioni. Se viene chiamato <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> (in modo annidato, ovvero nella stessa sessione senza commit o rollback) il numero di volte di questo valore, nell'ultima chiamata JET_errTransTooDeep verrà restituito da <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>. Si noti che il valore in Windows 2000, Windows XP e Windows Server 2003 è 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoVersion</p></td>
<td><p><em>pvResult</em> verrà interpretato come Long. Viene restituita la versione principale nativa del motore di database. Questo valore è 0x620 per Windows 2000, Windows XP e Windows Server 2003.</p></td>
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
<td><p>La dimensione del buffer specificata in <em>cbMax</em> è troppo piccola (o non corretta) per conservare le informazioni desiderate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Il <em>InfoLevel</em> richiesto è stato JET_DbInfoIsam. Questo non è supportato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>La dimensione del buffer specificata in <em>cbMax</em> è troppo piccola (o non corretta) per conservare le informazioni desiderate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo errore viene restituito da <strong>JetGetDatabaseInfo</strong> quando il <a href="gg269248(v=exchg.10).md">JET_DBID</a> specificato non è un database valido (collegato). Questo errore viene restituito da <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> e <strong>JetGetDatabaseInfo</strong> quando un <em>InfoLevel</em> richiesto non è supportato da tale versione della funzione.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, i dati richiesti verranno restituiti nel buffer di output.

In caso di errore, il buffer di output sarà in uno stato non definito.

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
<td><p>Implementato come <strong>JetGetDatabaseInfoW</strong> (Unicode) e <strong>JetGetDatabaseInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
