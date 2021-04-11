---
description: 'Altre informazioni su: funzione JetStopBackupInstance'
title: JetStopBackupInstance (funzione)
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128631"
---
# <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance (funzione)

La funzione **JetStopBackupInstance** impedisce che l'attività correlata al backup di flusso continui su un'istanza in esecuzione specifica, chiudendo in tal modo il backup del flusso in modo prevedibile.

**Windows XP:**  **JetStopBackupInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Identifica l'istanza in esecuzione da usare per la chiamata API.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Il valore del parametro di istanza specificato non è valido (non è un'istanza attualmente in esecuzione).</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, l'istanza specificata non riuscirà a eseguire alcuna nuova API di backup di flusso.

Se questa funzione ha esito negativo, non verrà eseguito alcun passaggio per preparare la terminazione del backup nell'istanza e non si verificherà alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Il backup viene in genere attivato da un evento esterno al meccanismo di processo e tramite questa API, l'applicazione ESENT stessa effettuerà altre chiamate alle API di backup di flusso per avere esito negativo. La maggior parte delle API di backup di flusso inizierà a non riuscire con JET_errBackupAbortByServer. Di conseguenza, lo stato di avanzamento del backup di flusso, ad esempio [JetReadFileInstance](./jetreadfileinstance-function.md), restituirà un errore. Verranno comunque consentite le operazioni di backup che fanno parte della terminazione del backup (ad esempio [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)).

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
