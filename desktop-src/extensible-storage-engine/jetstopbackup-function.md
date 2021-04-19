---
description: 'Altre informazioni su: funzione JetStopBackup'
title: JetStopBackup (funzione)
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323797"
---
# <a name="jetstopbackup-function"></a>JetStopBackup (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopbackup-function"></a>JetStopBackup (funzione)

La funzione **JetStopBackup** impedisce a tutte le attività correlate al backup di flusso di continuare su un'istanza in esecuzione specifica, chiudendo in tal modo il backup di flusso in modo prevedibile.

**Windows XP:**  Questa funzione è stata introdotta in Windows XP.

[JetStopService](./jetstopservice-function.md) è la chiamata legacy quando è consentita una sola istanza. In questo caso, l'unica istanza attiva è quella preparata per la terminazione.

```cpp
JET_ERR JET_API JetStopBackup(void);
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
<td><p>Non è chiaro quale istanza preparare per la terminazione quando si usa <a href="gg269240(v=exchg.10).md">JetStopService</a> con più modalità di istanza.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, l'istanza di avrà esito negativo per le nuove API di backup di flusso.

Se questa funzione ha esito negativo, non verrà eseguito alcun passaggio per preparare la terminazione del backup nell'istanza e non si verificherà alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Il backup viene in genere attivato da un evento esterno al meccanismo di processo e tramite questa API, l'applicazione ESENT stessa effettuerà altre chiamate alle API di backup di flusso per avere esito negativo. La maggior parte delle API di backup di flusso inizierà a non riuscire con JET_errBackupAbortByServer. Di conseguenza, lo stato di avanzamento del backup di flusso, ad esempio [JetReadFileInstance](./jetreadfileinstance-function.md), restituirà un errore. Verranno comunque consentite le operazioni di backup che fanno parte della terminazione del backup, ad esempio [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md).

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

[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
