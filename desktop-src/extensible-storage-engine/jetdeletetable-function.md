---
description: 'Altre informazioni su: Funzione JetDeleteTable'
title: Funzione JetDeleteTable
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cdac49d766835a0d26a3b9d474b8759a552ed1d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984904"
---
# <a name="jetdeletetable-function"></a>Funzione JetDeleteTable


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeletetable-function"></a>Funzione JetDeleteTable

La **funzione JetDeleteTable** elimina una tabella in un database ESE.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*Dbid*

Identificatore del database da usare per la chiamata API.

*szTableName*

Nome della tabella da eliminare.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errTableInUse</p> | <p>Si è tentato di eliminare una tabella mentre un'altra sessione ha un ID di tabella aperto (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) con <a href="gg294118(v=exchg.10).md">JetOpenTable</a> o <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</p> | 
| <p>JET_errCannotDeletetemporary tabella</p> | <p>Si è tentato di eliminare una tabella temporanea. Una tabella temporanea viene eliminata automaticamente quando viene chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable.</a></p> | 
| <p>JET_errCannotDeleteTemplateTable</p> | <p>Si è tentato di eliminare una tabella modello, ovvero una tabella da cui è possibile ereditare DDL.</p> | 



#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDeleteTableW</strong> (Unicode) e <strong>JetDeleteTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)
