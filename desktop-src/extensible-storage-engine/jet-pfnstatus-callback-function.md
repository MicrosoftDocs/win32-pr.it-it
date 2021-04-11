---
description: 'Altre informazioni su: JET_PFNSTATUS funzione di callback'
title: Funzione di callback JET_PFNSTATUS
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232561"
---
# <a name="jet_pfnstatus-callback-function"></a>Funzione di callback JET_PFNSTATUS


_**Si applica a:** Windows | Windows Server_

## <a name="jet_pfnstatus-callback-function"></a>Funzione di callback JET_PFNSTATUS

La funzione di callback **JET_PFNSTATUS** riceve informazioni sullo stato di avanzamento delle operazioni a esecuzione prolungata, ad esempio operazioni di deframmentazione, backup o ripristino. Durante tali operazioni, il motore di database chiama questa funzione di callback per fornire un aggiornamento sullo stato di avanzamento dell'operazione.

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

Sessione di tipo [JET_SESID](./jet-sesid.md) con la quale è stata chiamata la funzione a esecuzione prolungata.

*SNP*

Tipo di operazione come specificato in [JET_SNP](./jet-snp.md). I tipi di operazioni includono ripristino, compattazione, ripristino, backup, aggiornamento, scrub e aggiornamento del formato di record.

*SNT*

Stato di un'operazione. I tipi di stato includono inizio, in corso, completamento o errore. Lo stato verrà specificato con il terzo parametro di tipo [JET_SNT](./jet-snt.md).

*PV*

Puntatore facoltativo a una struttura di tipo [JET_SNPROG](./jet-snprog-structure.md).

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei [codici di errore Extensible Storage Engine](./extensible-storage-engine-error-codes.md). Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

In seguito all'esito positivo, l'operazione che ha emesso il callback può procedere normalmente. In alcuni casi, il callback potrebbe restituire un avviso che influenza l'operazione.

In caso di errore, l'operazione che ha emesso il callback potrebbe procedere normalmente o potrebbe non riuscire.

### <a name="remarks"></a>Commenti

Questa funzione di callback verrà utilizzata in una notifica di stato in cui la struttura indicherà lo stato corrente dello stato di avanzamento. Si noti che la funzione di callback potrebbe essere chiamata più volte per lo stato di avanzamento dell'operazione.

### <a name="requirements"></a>Requisiti

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
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[Codici di errore di Extensible Storage Engine](./extensible-storage-engine-error-codes.md)  
[Errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_SESID](./jet-sesid.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
