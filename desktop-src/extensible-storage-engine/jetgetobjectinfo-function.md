---
description: Altre informazioni sulla funzione JetGetObjectInfo
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
ms.openlocfilehash: 824c19fbb1fb1e479b805eb45bf8ff56458110d0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469788"
---
# <a name="jetgetobjectinfo-function"></a>Funzione JetGetObjectInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetobjectinfo-function"></a>Funzione JetGetObjectInfo

La **funzione JetGetObjectInfo** recupera informazioni sugli oggetti di database. Attualmente sono supportate solo le tabelle. [JetGetTableInfo può](./jetgettableinfo-function.md) essere usato per recuperare più informazioni rispetto **a JetGetObjectInfo.**

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

*Dbid*

Database da cui vengono recuperate le informazioni.

*objtyp*

Oggetti che contengono informazioni da recuperare. Attualmente sono supportati solo JET_objtypNil e JET_objtypTable, entrambi si comportano in modo identico. Verranno recuperate solo le tabelle.

*szContainerName*

Questo parametro è riservato per un uso futuro e passa **NULL.** Nome dei tipi di oggetti sui quali recuperare le informazioni.

*szObjectName*

Nome dell'oggetto che contiene le informazioni da recuperare. Quando *InfoLevel* usa le opzioni JET_ObjInfoList o JET_ObjInfoListNoStats per recuperare un elenco di tutti gli oggetti, questo valore deve essere **NULL** o una stringa vuota.

Sono attualmente supportati solo i nomi di tabella.

*pvResult*

Puntatore a un buffer che riceve le informazioni specificate.

Le dimensioni del buffer, in byte, vengono passate in *cbMax*. In caso di errore, il contenuto *di pvResult* non è definito.

Le informazioni archiviate in *pvResult* dipendono da *InfoLevel*.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult.*

*InfoLevel*

Specifica il tipo di informazioni da recuperare per l'oggetto specificato. Influisce sul modo *in cui viene interpretato pvResult.*

Per questo parametro sono disponibili le opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_ObjInfo</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> struttura.</p><p>La <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> struttura viene popolata con le informazioni relative all'oggetto denominato in <em>szObjectName</em>.</p><p>Se il chiamante non vuole conoscere il numero di record e pagine per l'oggetto, provare JET_ObjInfoNoStats livello di informazioni, che potrebbe essere più veloce perché le statistiche non sono incluse.</p> | 
| <p>JET_ObjInfoList</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> struttura. Vengono recuperate informazioni su tutti gli oggetti. Verrà creata una tabella temporanea e le informazioni necessarie per attraversare la tabella temporanea sono descritte nella JET_OBJECTLIST <a href="gg269348(v=exchg.10).md">struttura.</a> Per altre informazioni, <a href="gg269348(v=exchg.10).md">vedere</a>JET_OBJECTLIST . Se il chiamante non vuole conoscere il numero di record e pagine per l'oggetto, è consigliabile usare JET_ObjInfoListNoStats, che potrebbe essere più veloce.</p> | 
| <p>JET_ObjInfoListACM</p> | <p>Deprecato e attualmente non supportato.</p> | 
| <p>JET_ObjInfoListNoStats</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> struttura. Vengono recuperate informazioni su tutti gli oggetti. Verrà creata una tabella temporanea e le informazioni necessarie per attraversare la tabella temporanea sono descritte nella JET_OBJECTLIST <a href="gg269348(v=exchg.10).md">struttura.</a> Per altre informazioni, <a href="gg269348(v=exchg.10).md">vedere</a>JET_OBJECTLIST . JET_ObjInfoListNoStats è identico JET_ObjInfoList, ad eccezione del fatto che le colonne che segnalano il numero di record (<em>columnidcRecord</em>) e le pagine (<em>columnidcPage</em>) non verranno aggiornate.</p> | 
| <p>JET_ObjInfoMax</p> | <p><em>pvResult viene</em> interpretato come un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Le dimensioni massime dell'oggetto sono in pagine. Attualmente verranno restituite solo le tabelle.</p> | 
| <p>JET_ObjInfoNoStats</p> | <p><em>pvResult viene</em> interpretato come un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Verranno recuperate solo le informazioni sull'oggetto specificato in <em>szObjectName.</em></p><p>La <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> verrà popolata con le informazioni relative all'oggetto denominato in <em>szObjectName</em>.</p><p>JET_ObjInfoNoStats è identico a JET_ObjInfo, ad eccezione del fatto che i campi che segnalano il numero di record e pagine sono impostati su zero.</p> | 
| <p>JET_ObjInfoRulesLoaded</p> | <p>Deprecato e attualmente non supportato.</p> | 
| <p>JET_ObjInfoSysTabCursor</p> | <p>Deprecato e attualmente non supportato.</p> | 
| <p>JET_ObjInfoSysTabReadOnly</p> | <p>Deprecato e attualmente non supportato.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Le dimensioni del buffer specificate in <em>cbMax</em> erano troppo piccole per contenere le informazioni desiderate.</p> | 
| <p>JET_errInvalidName</p> | <p>È stato specificato un nome non valido in <em>szObjectName</em> o <em>szContainerName</em>.</p> | 
| <p>JET_errInvalidParameter</p> | <p>È stato specificato un parametro non valido. È possibile che sia stato passato un livello non valido a <em>InfoLevel</em>.</p> | 



#### <a name="remarks"></a>Commenti

Se **JetGetObjectInfo** crea correttamente una tabella temporanea (ad esempio, JET_ObjInfoList o JET_ObjInfoNoStats), il chiamante è responsabile della chiusura della tabella temporanea [con JetCloseTable](./jetclosetable-function.md).

**JetGetObjectInfo** attualmente supporta solo il recupero di informazioni sulle tabelle.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetObjectInfoW</strong> (Unicode) e <strong>JetGetObjectInfoA</strong> (ANSI).</p> | 



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
