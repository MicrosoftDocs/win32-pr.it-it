---
description: Altre informazioni sulla funzione JetGetIndexInfo
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
ms.openlocfilehash: e4d7c835d5077d2bfee87025b202480a888de981
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988584"
---
# <a name="jetgetindexinfo-function"></a>Funzione JetGetIndexInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetindexinfo-function"></a>Funzione JetGetIndexInfo

La **funzione JetGetIndexInfo** recupera informazioni su un indice.

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

*Dbid*

Identificatore del database da usare per la chiamata API.

*szTableName*

Nome della tabella contenente l'indice con le informazioni da recuperare.

*szIndexName*

Nome dell'indice con le informazioni da recuperare.

*pvResult*

Puntatore a un buffer che riceverà le informazioni desiderate. Il buffer deve essere allineato per contenere il tipo richiesto. Il tipo del buffer dipende dal *parametro InfoLevel.*

*cbResult*

Dimensione, in byte, del buffer passato come *pvResult.*

*InfoLevel*

Informazioni che verranno archiviate in *pvResult.* Per questo parametro è possibile usare le opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> struttura. In caso di esito <a href="gg269185(v=exchg.10).md">positivo, JET_INDEXLIST</a> struttura riceve informazioni sull'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>pvResult viene</em> interpretato come ULONG. In caso di esito positivo, ULONG contiene il conteggio degli indici nella tabella specificata. <em>szIndexName viene</em> ignorato. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>pvResult viene</em> interpretato come un <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. In caso di esito <a href="gg269327(v=exchg.10).md">positivo, JET_INDEXID</a> struttura riceve informazioni sull'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid deprecato. Usare JET_IdxInfoLCID e la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID.</a></p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>pvResult viene</em> interpretato come LCID. In caso di esito positivo, l'LCID contiene l'identificatore delle impostazioni locali dell'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p><p><strong>Windows XP:</strong> JET_IdxInfoLCID è stato introdotto in Windows XP.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> struttura. In caso di esito <a href="gg269185(v=exchg.10).md">positivo, JET_INDEXLIST</a> struttura riceve informazioni sull'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC è obsoleto.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC è obsoleto.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>pvResult viene</em> interpretato come ULONG. In caso di esito positivo, ULONG contiene l'utilizzo dello spazio dell'indice. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor è obsoleto.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>pvResult viene</em> interpretato come USHORT. In caso di esito positivo, USHORT contiene il valore <em>di cbVarSegMac</em> usato al momento della creazione dell'indice. Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per una descrizione di <em>cbVarSegMac</em>. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>pvResult viene</em> interpretato come USHORT. In caso di esito positivo, USHORT contiene il valore <em>di cbKeyMost</em> usato al momento della creazione dell'indice. Vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> per una descrizione di <em>cbKeyMost</em>. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p><p><strong>Windows Vista:</strong> JET_IdxInfoKeyMost è stato introdotto in Windows Vista.</p> | 
| <p>JET_IdxInfoCreateIndex</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> struttura. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex è stato introdotto in Windows 7.</p> | 
| <p>JET_IdxInfoCreateIndex2</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> struttura. In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</p><p><strong>Windows 7:</strong> JET_IdxInfoCreateIndex2 è stato introdotto in Windows 7.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errIndexNotFound</p> | <p>Impossibile trovare l'indice specificato nella tabella specificata.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Il buffer passato come <em>pvResult</em> era troppo piccolo. Il contenuto del buffer non è definito.</p> | 



#### <a name="remarks"></a>Commenti

**JetGetIndexInfo e** [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperano informazioni identiche su un indice. La differenza è nel modo in cui viene specificata la tabella. **JetGetIndexInfo** prevede un database (*dbid*) e il nome di una tabella (*szTableName*), mentre [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) prevede un identificatore di tabella (*tableid*).

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetIndexInfoW</strong> (Unicode) e <strong>JetGetIndexInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
