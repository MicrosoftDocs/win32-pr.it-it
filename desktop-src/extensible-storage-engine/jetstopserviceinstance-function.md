---
description: Altre informazioni sulla funzione JetStopServiceInstance
title: Funzione JetStopServiceInstance
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
ms.openlocfilehash: e82f7b3ea85ffb76f58dd0ada8c56b83ecdf40a4b40e799b7ae482f307d1f916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614631"
---
# <a name="jetstopserviceinstance-function"></a>Funzione JetStopServiceInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopserviceinstance-function"></a>Funzione JetStopServiceInstance

La **funzione JetStopServiceInstance** prepara un'istanza per la terminazione.

**Windows XP:****JetStopServiceInstance** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parametri

*Istanza*

Istanza in esecuzione da usare per la chiamata API.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Errori del motore Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).

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
<td><p>Il parametro di istanza specificato ha un valore non valido (non un'istanza attualmente in esecuzione).</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, si prepara per una terminazione futura. I passaggi eserciti per preparare una terminazione includono:

  - Arrestare la deframmentazione online se è in esecuzione.

  - Avviare una pulizia dell'archivio versioni.

  - Ridurre la profondità del checkpoint iniziando a scaricare le pagine dirty nella gestione buffer.

  - Impedire chiamate future alla maggior parte delle funzioni per tale istanza.

Se questa funzione ha esito negativo, non verrà eseguito alcun processo di preparazione per la terminazione di un'istanza, quindi non verrà apportata alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Questa funzione ridurrà il lavoro che l'istanza dovrà eseguire quando viene terminata, ma non termina l'istanza. Di conseguenza, questa funzione è solo un'ottimizzazione e non è obbligatoria da usare. Si noti che la quantità di lavoro svolto in preparazione è stata inferiore Windows 2000 e Windows XP. Al termine della funzione, la chiamata di funzioni che non sono più consentite restituirà JET_errClientRequestToStopJetService. Le funzioni ancora consentite dopo questa chiamata sono: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) [e JetResetSessionContext](./jetresetsessioncontext-function.md).

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
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
