---
title: Tipi di dati nap (NapTypes.h)
description: Nota La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10 I tipi di dati per l'API Protezione accesso alla rete sono i seguenti.
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- Tempo di prova
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Percentuale
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550baa14779ccefaec14605938edb6076e7cc332aa9d1a2390ab430f7568e844
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802621"
---
# <a name="nap-datatypes"></a>Tipi di dati di Protezione accesso alla rete

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

I tipi di dati per l'API Protezione accesso alla rete sono i seguenti.


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

**Tempo di prova**
</dt> <dd>

Struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che contiene un'ora correlata alla prova di un computer client.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Valore che specifica l'intervallo di valori possibili per le dimensioni massime, in byte, di un pacchetto [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) come definito da [**range( minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).

</dd> <dt>

**NapComponentId**
</dt> <dd>

Identificatore univoco a 4 byte usato da SHA, SHV e client di imposizione per identificarsi. I primi tre byte sono il codice SMI assegnato da IETF del fornitore e l'ultimo byte identifica il componente stesso.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Valore **NapComponentId** usato per identificare le coppie SHA/SHV.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Valore **NapComponentId** usato per identificare i client di imposizione.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Valore che specifica il numero di sha registrati nel sistema di Protezione accesso alla rete nell'intervallo da 0 (zero) a [**maxSystemHealthEntityCount.**](nap-type-constants.md)

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Valore che specifica il numero di client di imposizione nel sistema di Protezione accesso alla rete nell'intervallo da 0 (zero) a [**maxEnforcerCount.**](nap-type-constants.md)

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

Versione [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) di una [**struttura CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) usata per associare [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) a **SoHResponses**.

</dd> <dt>

**ConnectionId**
</dt> <dd>

Identificatore univoco univoco globale (GUID) usato per identificare le connessioni di Protezione accesso alla rete gestite dai client di imposizione.

</dd> <dt>

**Percentuale**
</dt> <dd>

Valore che contiene la percentuale compresa tra 0 (zero) e 100 di correzione completata

</dd> <dt>

**Messageid**
</dt> <dd>

Valore univoco utilizzato per identificare i messaggi di sistema di Protezione accesso alla rete.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                                                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt> </dl> |



 

