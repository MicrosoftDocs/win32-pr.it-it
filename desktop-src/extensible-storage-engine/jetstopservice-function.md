---
description: 'Altre informazioni su: funzione JetStopService'
title: Funzione JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307806"
---
# <a name="jetstopservice-function"></a>Funzione JetStopService


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopservice-function"></a>Funzione JetStopService

La funzione **JetStopService** prepara un'istanza per la chiusura.

**JetStopService** è la chiamata legacy quando è consentita una sola istanza. In questo caso, l'unica istanza attiva è quella preparata per la terminazione.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Non è chiaro quale istanza preparare per la terminazione quando si usa <strong>JetStopService</strong> con più modalità di istanza.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, viene preparata per una terminazione futura. I passaggi necessari per preparare la chiusura includono i seguenti:

  - Arrestare la deframmentazione in linea se è in esecuzione.

  - Avviare una pulizia dell'archivio versioni.

  - Per ridurre la profondità del checkpoint, iniziare a scaricare le pagine dirty in Gestione buffer.

  - Evitare chiamate future alla maggior parte delle funzioni per l'istanza.

Se questa funzione ha esito negativo, non verrà eseguita alcuna procedura per preparare la terminazione di un'istanza, quindi non si verificherà alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Questa funzione riduce il lavoro che l'istanza dovrà eseguire quando viene terminata, ma non termina l'istanza. Di conseguenza, questa funzione è solo un'ottimizzazione e non è obbligatoria per l'uso di. Si noti che la quantità di lavoro svolto in preparazione era minore in Windows 2000 e Windows XP. Quando la funzione ha esito positivo, la chiamata di funzioni che non sono più consentite restituirà JET_errClientRequestToStopJetService. Le funzioni ancora consentite dopo questa chiamata sono: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

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
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
