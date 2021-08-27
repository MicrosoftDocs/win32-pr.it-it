---
description: Altre informazioni sulla funzione JetDeleteIndex
title: Funzione JetDeleteIndex
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4170bd4def6ad60953189923252e2d775765b03d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478017"
---
# <a name="jetdeleteindex-function"></a>Funzione JetDeleteIndex


_**Si applica a:** Windows | Windows Server_

## <a name="jetdeleteindex-function"></a>Funzione JetDeleteIndex

La **funzione JetDeleteIndex** elimina un indice da una tabella.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*tableid*

Tabella contenente la colonna da eliminare.

*szIndexName*

Nome dell'indice da eliminare.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errFixedDDL</p> | <p>Si è tentato di eliminare un indice da una tabella fissa, ad esempio uno creato con JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Si è tentato di eliminare un indice da una tabella modello. Una tabella modello ha una DDL fissa.</p> | 
| <p>JET_errIndexNotFound</p> | <p>Impossibile trovare l'indice denominato in <em>szIndexName.</em></p> | 
| <p>JET_errPermissionDenied</p> | <p>Impossibile aggiornare la tabella perché è stata aperta in sola lettura.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Più thread hanno tentato di usare la stessa sessione di database.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transazione è stata aperta come transazione di sola lettura.</p> | 



#### <a name="remarks"></a>Commenti

In caso di esito positivo, l'indice viene eliminato e pertanto non può essere utilizzato successivamente. Non deve essere presente alcuna transazione attiva che utilizza l'indice.

In caso di esito positivo, la valuta viene impostata prima del primo record.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetDeleteIndexW</strong> (Unicode) e <strong>JetDeleteIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)
