---
description: 'Altre informazioni su: funzione JET_PFNSTATUS callback'
title: JET_PFNSTATUS di callback
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d10de8491379a3e19217bcdb4a28f3546ebc009f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482917"
---
# <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS di callback


_**Si applica a:** Windows | Windows Server_

## <a name="jet_pfnstatus-callback-function"></a>JET_PFNSTATUS di callback

La **JET_PFNSTATUS** di callback riceve informazioni sullo stato di avanzamento delle operazioni a esecuzione lunga, ad esempio operazioni di deframmentazione, backup o ripristino. Durante queste operazioni, il motore di database chiama questa funzione di callback per fornire un aggiornamento sullo stato dell'operazione.

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione di tipo [JET_SESID](./jet-sesid.md) con cui è stata chiamata la funzione a esecuzione lunga.

*Snp*

Tipo di operazione specificato [in](./jet-snp.md)JET_SNP . I tipi di operazioni includono ripristino, compattazione, ripristino, backup, aggiornamento, scrub e aggiornamento del formato di record.

*Snt*

Stato di un'operazione. I tipi di stato includono inizio, in corso, completamento o errore. Lo stato verrà specificato con il terzo parametro di [tipo JET_SNT](./jet-snt.md).

*Pv*

Puntatore facoltativo a una struttura di tipo [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [tipo JET_ERR](./jet-err.md) dati con uno dei codici di errore del motore [Archiviazione extensible](./extensible-storage-engine-error-codes.md). Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).

In caso di esito positivo, l'operazione che ha eseguito il callback può procedere normalmente. In alcuni casi, il callback potrebbe restituire un avviso che influisce su tale operazione.

In caso di errore, l'operazione che ha eseguito il callback potrebbe continuare normalmente o potrebbe non riuscire.

### <a name="remarks"></a>Commenti

Questa funzione di callback verrà usata in una notifica di stato in cui la struttura indicherà lo stato corrente dello stato di avanzamento. Si noti che la funzione di callback potrebbe essere chiamata più volte per lo stato di avanzamento dell'operazione.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[Codici di errore del motore Archiviazione estendibile](./extensible-storage-engine-error-codes.md)  
[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
