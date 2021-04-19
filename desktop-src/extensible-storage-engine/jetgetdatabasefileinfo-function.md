---
description: 'Altre informazioni su: funzione JetGetDatabaseFileInfo'
title: JetGetDatabaseFileInfo (funzione)
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319632"
---
# <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo (funzione)

La funzione **JetGetDatabaseFileInfo** recupera vari tipi di informazioni sul database. Questa API può essere chiamata quando un database è collegato o in linea (con [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) o mentre il database o il motore di database è offline (con **JetGetDatabaseFileInfo**).

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*szDatabaseName*

Percorso del database da cui recuperare le informazioni.

*pvResult*

Puntatore a un buffer che riceverà le informazioni specificate. La dimensione del buffer, in byte, viene passata in *cbMax*.

Se questa funzione ha esito negativo, il contenuto di *pvResult* non è definito.

Le informazioni archiviate in *pvResult* dipendono da *InfoLevel*.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult*.

*InfoLevel*

*InfoLevel* specifica il tipo di informazioni da recuperare sul database specificato. Influiscono sul modo in cui *pvResult* viene interpretato. Alcuni oggetti *InfoLevel* sono disponibili solo nella versione offline (**JetGetDatabaseFileInfo**) o in linea ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) dell'API.

Se il buffer di *pvResult* fornito è troppo piccolo, viene restituito JET_errInvalidBufferSize o JET_errBufferTooSmall, a seconda del valore di *InfoLevel*.

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
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> verrà interpretato come QWORD (8 byte). Restituisce le dimensioni in byte del database.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvResult</em> verrà interpretato come <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>. La struttura di <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> verrà popolata con le informazioni relative al database specificato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> verrà interpretato come <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La struttura di <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> verrà popolata con le informazioni relative al database specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvResult</em> verrà interpretato come bool (4 byte). Verrà restituito un valore che indica se il motore di database dispone attualmente di database aperti o collegati.</p>
<p><strong>Windows XP:  </strong> Questo valore è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvResult</em> verrà interpretato come unsigned long. Questa operazione restituirà le dimensioni di pagina del database in byte.</p>
<p><strong>Windows XP:  </strong> Questo valore è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Questi <em>InfoLevels</em> non sono ancora supportati e restituiscono valori predefiniti. Non usare questi <em>InfoLevels</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Questi <em>InfoLevels</em> non sono ancora supportati e restituiscono valori predefiniti. Non usare questi <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>Uguale a JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Questi <em>InfoLevels</em> sono deprecati e non sono attualmente supportati. Non usare questi <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Uguale a JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista:  </strong> Questo valore <em>InfoLevel</em> è stato introdotto in Windows Vista.</p>
<p><em>pvResult</em> verrà considerato un puntatore a un valore DWORD. Restituisce un valore di enumerazione che indica il tipo di file considerato dal motore. I tipi di file sono elencati nella tabella seguente. Per altre informazioni su questi tipi di file e sul relativo utilizzo al motore, vedere <a href="gg294069(v=exchg.10).md">file del motore di archiviazione estensibile</a>.</p>
<div class="tableSection">
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
<td><p>JET_filetypeUnknown</p></td>
<td><p>Il tipo di file è sconosciuto o non è un tipo di file ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>Il file è un file di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>Il file è un file di log delle transazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>Il file è un file del checkpoint.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeTempDatabase</p></td>
<td><p>Il file è un file di database temporaneo.</p></td>
</tr>
</tbody>
</table>

</div></td>
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
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Il <em>InfoLevel</em> richiesto è stato JET_DbInfoIsam. Questo non è supportato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Il buffer fornito in <em>cbMax</em> è troppo piccolo per le informazioni desiderate.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Il buffer fornito in <em>cbMax</em> non è la dimensione corretta per le informazioni desiderate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto. Questo errore viene restituito da <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando DBID specificato non è un database valido (collegato). Questo errore viene restituito da <strong>JetGetDatabaseFileInfo</strong> e <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando un <em>InfoLevel</em> richiesto non è supportato da tale versione della funzione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, i dati richiesti verranno restituiti nel buffer di output.

Se questa funzione ha esito negativo, il buffer di output sarà in uno stato non definito.

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
<td><p>Implementato come <strong>JetGetDatabaseFileInfoW</strong> (Unicode) e <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)
