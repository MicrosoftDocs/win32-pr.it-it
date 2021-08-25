---
description: Altre informazioni sulla funzione JetStopService
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
ms.openlocfilehash: 75e8622d79f2757bee8ab3041250b2ba78499194
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480307"
---
# <a name="jetstopservice-function"></a>Funzione JetStopService


_**Si applica a:** Windows | Windows Server_

## <a name="jetstopservice-function"></a>Funzione JetStopService

La **funzione JetStopService** prepara un'istanza per la terminazione.

**JetStopService è** la chiamata legacy quando è consentita una sola istanza. In questo caso, l'unica istanza attiva è quella preparata per la terminazione.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Non è chiaro quale istanza preparare per la terminazione quando si usa <strong>JetStopService</strong> con la modalità a istanza multipla.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 



Se questa funzione ha esito positivo, si prepara per una terminazione futura. Di seguito sono riportati i passaggi necessari per preparare una chiusura:

  - Arrestare la deframmentazione online se è in esecuzione.

  - Avviare la pulizia di un archivio versioni.

  - Ridurre la profondità del checkpoint iniziando a scaricare le pagine dirty in Gestione buffer.

  - Impedire chiamate future alla maggior parte delle funzioni per tale istanza.

Se questa funzione ha esito negativo, non verrà eseguito alcuno dei passaggi per preparare la terminazione di un'istanza, quindi non verrà apportata alcuna modifica allo stato dell'istanza.

#### <a name="remarks"></a>Commenti

Questa funzione riduce il lavoro che l'istanza dovrà eseguire quando viene terminata, ma non termina l'istanza. Di conseguenza, questa funzione è solo un'ottimizzazione e non è obbligatoria da usare. Si noti che la quantità di lavoro svolto in preparazione è stata inferiore Windows 2000 e Windows XP. Una volta che la funzione ha esito positivo, la chiamata di funzioni che non sono più consentite restituirà JET_errClientRequestToStopJetService. Le funzioni ancora consentite dopo questa chiamata sono: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



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
