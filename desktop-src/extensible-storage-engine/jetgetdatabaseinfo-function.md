---
description: Altre informazioni sulla funzione JetGetDatabaseInfo
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
ms.openlocfilehash: 335ad13411dbfcc83dce559eb4b77adefcc8a5da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477957"
---
# <a name="jetgetdatabaseinfo-function"></a>Funzione JetGetDatabaseInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetdatabaseinfo-function"></a>Funzione JetGetDatabaseInfo

La **funzione JetGetDatabaseInfo** recupera vari tipi di informazioni sul database. Questa API può essere chiamata mentre un database è collegato o online (con **JetGetDatabaseInfo**) o mentre il database o il motore di database è offline (con [JetGetDatabaseFileInfo).](./jetgetdatabasefileinfo-function.md)

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

*Dbid*

Oggetto [JET_DBID](./jet-dbid.md) il database da cui recuperare le informazioni.

*pvResult*

Puntatore a un buffer che riceverà le informazioni specificate. Le dimensioni del buffer, in byte, vengono passate in *cbMax*.

In caso di errore, il contenuto *di pvResult* non è definito.

Le informazioni archiviate in *pvResult* dipendono da *InfoLevel.*

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult.*

*InfoLevel*

*InfoLevel* specifica il tipo di informazioni da recuperare sul database specificato. Influisce sulla modalità *di interpretazione di pvResult.* Alcuni *InfoLevel* sono disponibili solo nella versione offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) o online (**JetGetDatabaseInfo**) dell'API.

Se il buffer *pvResult* specificato è troppo piccolo, JET_errInvalidBufferSize o JET_errBufferTooSmall verrà restituito a seconda di *InfoLevel.*


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_DbInfoCollate</p> | <p>Non ancora supportato e restituiscono valori predefiniti. Non usare.</p> | 
| <p>JET_DbInfoConnect</p> | <p>Questi <em>InfoLevel sono</em> deprecati e non sono attualmente supportati. Non usare.</p> | 
| <p>JET_DbInfoCountry</p> | <p>Non ancora supportato e restituiscono valori predefiniti. Non usare.</p> | 
| <p>JET_DbInfoCp</p> | <p>Non ancora supportato e restituiscono valori predefiniti. Non usare.</p> | 
| <p>JET_DbInfoFilename</p> | <p><em>pvResult</em> verrà interpretato come un buffer di stringa (char *). È MAX_PATH un buffer di dati, ma non obbligatorio. Se il buffer non è sufficientemente lungo, JET_errBufferTooSmall verrà restituito . La stringa verrà popolata con il percorso del database per questo DBID.</p> | 
| <p>JET_DbInfoFilesize</p> | <p><em>pvResult</em> verrà interpretato come DWORD (4 byte). Restituisce le dimensioni del database in pagine.</p> | 
| <p>JET_DbInfoIsam</p> | <p>Questi <em>InfoLevel sono</em> deprecati e non sono attualmente supportati. Non usare.</p> | 
| <p>JET_DbInfoLCID</p> | <p>(Windows XP e versioni successive) Questo <em>InfoLevel è</em> stato originariamente specificato come: JET_DbInfoLangid (Windows 2000)</p><p><em>pvResult</em> verrà interpretato come long. Viene restituito l'identificatore delle impostazioni locali (LCID) associato al database.</p> | 
| <p>JET_DbInfoMisc</p> | <p><em>pvResult</em> verrà interpretato come un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> verrà popolata con le informazioni relative al database specificato.</p> | 
| <p>JET_DbInfoOptions</p> | <p><em>pvResult</em> verrà interpretato come <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Restituisce un valore che indica se il database è aperto in modalità esclusiva. Se il database è in modalità JET_bitDbExclusive verrà <a href="gg294066(v=exchg.10).md"></a> impostato nel JET_GRBIT specificato, in caso contrario viene impostato zero. Si noti che non <em>vengono restituite</em> altre opzioni grbit del database <a href="gg294074(v=exchg.10).md">per JetAttachDatabase</a> e <a href="gg269299(v=exchg.10).md">JetOpenDatabase.</a></p> | 
| <p>JET_DbInfoPageSize</p> | <p>Disponibile solo in Windows XP e versioni successive. <em>pvResult</em> verrà interpretato come long senza segno. Verranno restituite le dimensioni della pagina del database in byte.</p> | 
| <p>JET_DbInfoSpaceAvailable</p> | <p><em>pvResult</em> verrà interpretato come DWORD. Viene restituito lo spazio disponibile per il database in pagine.</p> | 
| <p>JET_DbInfoSpaceOwned</p> | <p><em>pvResult</em> verrà interpretato come DWORD. In questo modo viene restituito lo spazio di proprietà per il database in pagine.</p> | 
| <p>JET_DbInfoTransactions</p> | <p><em>pvResult</em> verrà interpretato come long. Verrà restituito un valore maggiore del livello massimo al quale è possibile annidare le transazioni. Se <a href="gg294083(v=exchg.10).md">jetBeginTransaction</a> viene chiamato (in modalità di annidamento, ovvero nella stessa sessione, senza commit o rollback) tutte le volte che questo valore, all'ultima chiamata JET_errTransTooDeep verrà restituito <a href="gg294083(v=exchg.10).md">da JetBeginTransaction.</a> Si noti che il valore in Windows 2000, Windows XP e Windows Server 2003 è 7.</p> | 
| <p>JET_DbInfoVersion</p> | <p><em>pvResult</em> verrà interpretato come long. Viene restituita la versione principale nativa del motore di database. Questo valore è 0x620 per Windows 2000, Windows XP e Windows Server 2003.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>La dimensione del buffer specificata in <em>cbMax</em> era troppo piccola (o non corretta) per contenere le informazioni desiderate.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Il <em>valore InfoLevel</em> richiesto è JET_DbInfoIsam. Questo non è supportato.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>La dimensione del buffer specificata in <em>cbMax</em> era troppo piccola (o non corretta) per contenere le informazioni desiderate.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo errore verrà restituito <strong>da JetGetDatabaseInfo</strong> quando il <a href="gg269248(v=exchg.10).md">JET_DBID</a> specificato non è un database valido (collegato). Questo errore verrà restituito da <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> e <strong>JetGetDatabaseInfo</strong> quando un <em>InfoLevel</em> richiesto non è supportato da tale versione della funzione.</p> | 



In caso di esito positivo, i dati richiesti verranno restituiti nel buffer di output.

In caso di errore, il buffer di output sarà in uno stato non definito.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetDatabaseInfoW</strong> (Unicode) e <strong>JetGetDatabaseInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
