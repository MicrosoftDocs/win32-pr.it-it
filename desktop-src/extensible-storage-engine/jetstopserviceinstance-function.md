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
ms.openlocfilehash: 55f9a8c6e91a70e447f03bc19bcd191d01ba0e08
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984304"
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

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Il parametro di istanza specificato ha un valore non valido (non un'istanza attualmente in esecuzione).</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 



Se questa funzione ha esito positivo, si prepara per una terminazione futura. I passaggi eserciti per preparare una terminazione includono:

  - Arrestare la deframmentazione online se è in esecuzione.

  - Avviare una pulizia dell'archivio versioni.

  - Ridurre la profondità del checkpoint iniziando a scaricare le pagine dirty nella gestione buffer.

  - Impedire chiamate future alla maggior parte delle funzioni per tale istanza.

Se questa funzione ha esito negativo, non verrà eseguito alcun processo di preparazione per la terminazione di un'istanza, quindi non verrà apportata alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Questa funzione ridurrà il lavoro che l'istanza dovrà eseguire quando viene terminata, ma non termina l'istanza. Di conseguenza, questa funzione è solo un'ottimizzazione e non è obbligatoria da usare. Si noti che la quantità di lavoro svolto in preparazione è stata inferiore Windows 2000 e Windows XP. Al termine della funzione, la chiamata di funzioni che non sono più consentite restituirà JET_errClientRequestToStopJetService. Le funzioni che sono ancora consentite dopo questa chiamata sono: [JetRollback,](./jetrollback-function.md) [JetCloseTable,](./jetclosetable-function.md) [JetEndSession,](./jetendsession-function.md) [JetCloseDatabase,](./jetclosedatabase-function.md) [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext.](./jetresetsessioncontext-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



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
