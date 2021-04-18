---
description: 'Altre informazioni su: funzione JetGetObjectInfo'
title: Funzione JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313101"
---
# <a name="jetgetobjectinfo-function"></a>Funzione JetGetObjectInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetobjectinfo-function"></a>Funzione JetGetObjectInfo

La funzione **JetGetObjectInfo** recupera le informazioni sugli oggetti di database. Attualmente sono supportate solo le tabelle. [JetGetTableInfo](./jetgettableinfo-function.md) può essere usato per recuperare altre informazioni rispetto a **JetGetObjectInfo**.

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da utilizzare.

*dbid*

Database da cui vengono recuperate le informazioni.

*objtyp*

Oggetti che contengono informazioni da recuperare. Attualmente sono supportate solo JET_objtypNil e JET_objtypTable, entrambe comportano in modo identico. Verranno recuperate solo le tabelle.

*szContainerName*

Questo parametro è riservato per utilizzi futuri e passa **null**. Nome dei tipi di oggetti sui quali recuperare le informazioni.

*szObjectName*

Nome dell'oggetto che contiene le informazioni da recuperare. Quando *InfoLevel* usa le opzioni JET_ObjInfoList o JET_ObjInfoListNoStats per recuperare un elenco di tutti gli oggetti, questo valore deve essere **null** o una stringa vuota.

Attualmente sono supportati solo i nomi di tabella.

*pvResult*

Puntatore a un buffer che riceve le informazioni specificate.

La dimensione del buffer, in byte, viene passata in *cbMax*. In caso di errore, il contenuto di *pvResult* non è definito.

Le informazioni archiviate in *pvResult* dipendono da *InfoLevel*.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult*.

*InfoLevel*

Specifica il tipo di informazioni da recuperare per l'oggetto specificato. Influiscono sul modo in cui *pvResult* viene interpretato.

Le opzioni seguenti sono disponibili per l'impostazione di questo parametro.

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
<td><p>JET_ObjInfo</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</p>
<p>La struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> viene popolata con le informazioni relative all'oggetto denominato in <em>szObjectName</em>.</p>
<p>Se il chiamante non desidera determinare il numero di record e pagine per l'oggetto, è consigliabile utilizzare JET_ObjInfoNoStats livello di informazioni, che potrebbe essere più veloce poiché le statistiche non vengono incluse.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoList</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Vengono recuperate informazioni su tutti gli oggetti. Verrà creata una tabella temporanea e le informazioni necessarie per attraversare la tabella temporanea sono descritte nella struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Per ulteriori informazioni, vedere <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Se il chiamante non desidera ottenere informazioni sul numero di record e pagine per l'oggetto, provare a utilizzare JET_ObjInfoListNoStats, che potrebbe essere più veloce.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoListACM</p></td>
<td><p>Deprecato e attualmente non supportato.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoListNoStats</p></td>
<td><p><em>pvResult</em> viene interpretato come una struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Vengono recuperate informazioni su tutti gli oggetti. Verrà creata una tabella temporanea e le informazioni necessarie per attraversare la tabella temporanea sono descritte nella struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Per ulteriori informazioni, vedere <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats è identico a JET_ObjInfoList, ad eccezione del fatto che le colonne che segnalano il numero di record (<em>columnidcRecord</em>) e le pagine (<em>columnidcPage</em>) non verranno aggiornate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoMax</p></td>
<td><p><em>pvResult</em> viene interpretato come <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Le dimensioni massime dell'oggetto sono in pagine. Attualmente verranno restituite solo le tabelle.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoNoStats</p></td>
<td><p><em>pvResult</em> viene interpretato come <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Verranno recuperate solo le informazioni relative all'oggetto fornito in <em>szObjectName</em> .</p>
<p>La struttura di <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> verrà popolata con informazioni relative all'oggetto denominato in <em>szObjectName</em>.</p>
<p>JET_ObjInfoNoStats è identico a JET_ObjInfo, ad eccezione del fatto che i campi che segnalano il numero di record e le pagine sono impostati su zero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoRulesLoaded</p></td>
<td><p>Deprecato e attualmente non supportato.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoSysTabCursor</p></td>
<td><p>Deprecato e attualmente non supportato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoSysTabReadOnly</p></td>
<td><p>Deprecato e attualmente non supportato.</p></td>
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
<td><p>La dimensione del buffer specificata in <em>cbMax</em> è troppo piccola per conservare le informazioni desiderate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>È stato specificato un nome non valido in <em>szObjectName</em> o <em>szContainerName</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>È stato specificato un parametro non valido. È possibile che sia stato passato un livello non valido a <em>InfoLevel</em>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Se **JetGetObjectInfo** crea correttamente una tabella temporanea, ad esempio JET_ObjInfoList o JET_ObjInfoNoStats, il chiamante è responsabile della chiusura della tabella temporanea con [JetCloseTable](./jetclosetable-function.md).

**JetGetObjectInfo** supporta attualmente solo il recupero di informazioni sulle tabelle.

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
<td><p>Implementato come <strong>JetGetObjectInfoW</strong> (Unicode) e <strong>JetGetObjectInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
