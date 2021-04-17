---
description: 'Altre informazioni su: funzione JetStopServiceInstance'
title: JetStopServiceInstance (funzione)
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b2e3307f13a63d00cbbaf33f491750bbfcdb9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306211"
---
# <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance (funzione)

La funzione **JetStopServiceInstance** prepara un'istanza per la chiusura.

**Windows XP:**  **JetStopServiceInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza in esecuzione da usare per la chiamata API.

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


Se questa funzione ha esito positivo, viene preparata per una terminazione futura. I passaggi necessari per preparare la chiusura includono i seguenti:

  - Arrestare la deframmentazione in linea se è in esecuzione.

  - Avviare una pulizia dell'archivio versioni.

  - Per ridurre la profondità del checkpoint, iniziare a scaricare le pagine dirty in Gestione buffer.

  - Evitare chiamate future alla maggior parte delle funzioni per l'istanza.

Se questa funzione ha esito negativo, non verrà eseguita alcuna procedura per preparare la terminazione di un'istanza, quindi non si verificherà alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Questa funzione ridurrà il lavoro che l'istanza dovrà eseguire quando viene terminata, ma non verrà terminata l'istanza. Di conseguenza, questa funzione è solo un'ottimizzazione e non è obbligatoria per l'uso di. Si noti che la quantità di lavoro svolto in preparazione era minore in Windows 2000 e Windows XP. Quando la funzione ha esito positivo, la chiamata di funzioni che non sono più consentite restituirà JET_errClientRequestToStopJetService. Le funzioni ancora consentite dopo questa chiamata sono: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

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
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
