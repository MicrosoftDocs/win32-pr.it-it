---
description: Altre informazioni sulla funzione JetGetTableInfo
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
ms.openlocfilehash: 1c17e1c5aa23e8e2fe77aaa07f98fee1b2df0c12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465798"
---
# <a name="jetgettableinfo-function"></a>Funzione JetGetTableInfo


_**Si applica a:** Windows | Windows Server_

## <a name="jetgettableinfo-function"></a>Funzione JetGetTableInfo

La **funzione JetGetTableInfo** recupera varie informazioni su una tabella in un database.

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

*tableid*

Tabella a cui si applicano le informazioni.

*pvResult*

Puntatore a un buffer che riceverà le informazioni. Il tipo del buffer dipende da *InfoLevel.* È responsabilità del chiamante allineare il buffer in modo appropriato.

*cbMax*

Dimensione, in byte, del buffer passato in *pvResult.*

*InfoLevel*

Tipo di informazioni che verranno recuperate per la tabella specificata da *tableid*. Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel.*

Per questo parametro è possibile impostare le opzioni seguenti:


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_TblInfo</p> | <p><em>pvResult viene</em> interpretato come una <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> struttura. Se il metodo ha esito positivo, <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> struttura viene compilata con i dati appropriati. Se non riesce, il contenuto non è definito.</p> | 
| <p>JET_TblInfoDbid</p> | <p><em>pvResult viene</em> considerato come una matrice di <a href="gg269248(v=exchg.10).md">due</a> JET_DBID oggetti. L'identificatore di database del database proprietario della tabella viene archiviato due volte in questa matrice.</p> | 
| <p>JET_TblInfoDumpTable</p> | <p>JET_TblInfoDumpTable è deprecato. L'API restituirà JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoName</p> | <p>JET_TblInfoName recupera il nome della tabella e lo archivia in <em>pvResult.</em> Se il buffer è troppo piccolo, il comportamento non è definito.</p> | 
| <p>JET_TblInfoMostMany</p> | <p>JET_TblInfoMostMany recupera il nome della tabella e lo archivia in <em>pvResult.</em> Se il buffer è troppo piccolo, il comportamento non è definito.</p> | 
| <p>JET_TblInfoOLC</p> | <p>JET_TblInfoOLC deprecato. L'API restituirà JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoRvt</p> | <p>JET_TblInfoRvt è deprecato. L'API restituirà JET_errQueryNotSupported.</p> | 
| <p>JET_TblInfoResetOLC</p> | <p>JET_TblInfoResetOLC è deprecato. L'API restituirà JET_errFeatureNotAvailable.</p> | 
| <p>JET_TblInfoSpaceAlloc</p> | <p><em>pvResult viene</em> interpretato come una matrice di due gruppi ULONG:</p><ul><li><p>Il primo <strong>ULONG</strong> è il numero di pagine nella tabella.</p></li><li><p>Il secondo <strong>ULONG</strong> è la densità di destinazione delle pagine per la tabella.</p></li></ul> | 
| <p>JET_TblInfoSpaceAvailable</p> | <p><em>pvResult viene</em> interpretato come <strong>ULONG.</strong> <strong>ULONG</strong> è la somma del numero di pagine disponibili nella tabella, dei relativi indici e dell'albero dei valori lunghi.</p> | 
| <p>JET_TblInfoSpaceOwned</p> | <p><em>pvResult viene</em> interpretato come <strong>ULONG.</strong> <strong>ULONG</strong> è la somma del numero di pagine di proprietà della tabella (inclusi gli indici e l'albero dei valori lunghi e le eventuali pagine disponibili).</p> | 
| <p>JET_TblInfoSpaceUsage</p> | <p>Il comportamento dell'API dipende dalle dimensioni del buffer passato all'API. Due <em>valori cbMax</em> devono essere almeno ( 2 * sizeof( ULONG ) .</p><ul><li><p>Se <em>cbMax è</em> ( 2 * sizeof( ULONG ) ), <em>pvResult</em> viene interpretato come una matrice di due ULONG:</p><ul><li><p>Il primo <strong>ULONG</strong> è il numero di extent di proprietà della tabella.</p></li><li><p>Il secondo <strong>ULONG</strong> è il numero di extent disponibili della tabella.</p></li></ul></li><li><p><em>pvResult</em> viene interpretato come una matrice di:</p><ul><li><p>Il primo <strong>ULONG</strong> è il numero di extent di proprietà della tabella.</p></li><li><p>Il secondo <strong>ULONG</strong> è il numero di extent disponibili della tabella.</p></li></ul></li></ul> | 
| <p>JET_TblInfoTemplateTableName</p> | <p><em>pvResult viene</em> interpretato come buffer di stringa. Il buffer deve essere almeno JET_cbNameMost + 1, incluso il valore NULL di <strong>terminazione.</strong> Se la tabella è una tabella derivata, il buffer verrà compilato con il nome della tabella da cui la tabella derivata ha ereditato il DDL. Se la tabella non è una tabella derivata, il buffer sarà una stringa vuota.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Il buffer era troppo piccolo.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>È stato specificato <em>un InfoLevel</em> deprecato.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Le dimensioni del buffer non sono le giuste.</p> | 
| <p>JET_errInvalidOperation</p> | <p>La tabella passata è una tabella temporanea e non è possibile recuperare <em>infoLevel</em> richiesto per una tabella temporanea.</p> | 
| <p>JET_errObjectNotFound</p> | <p>La tabella passata è una tabella temporanea e non è possibile recuperare <em>infoLevel</em> richiesto per una tabella temporanea.</p> | 
| <p>JET_errQueryNotSupported</p> | <p><em>InfoLevel</em> non è supportato.</p> | 
| <p>JET_errTableInUse</p> | <p>La tabella viene utilizzata da un'altra operazione di database.</p> | 
| <p>JET_errTableLocked</p> | <p>La tabella è bloccata da un'altra operazione di database.</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>La tabella viene usata dal sistema. Questo avviso non è irreversibile.</p> | 



#### <a name="remarks"></a>Commenti

Alcune informazioni non sono valide per le tabelle temporanee (vedere [JetOpenTempTable](./jetopentemptable-function.md)).

Le statistiche della tabella includono il numero di record e il numero di pagine nell'indice cluster, ovvero l'indice contenente i dati del record. Le statistiche dell'indice sono accessibili separatamente in base al nome, [usando JetGetIndexInfo](./jetgetindexinfo-function.md) [o JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetGetTableInfoW</strong> (Unicode) e <strong>JetGetTableInfoA</strong> (ANSI).</p> | 



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
