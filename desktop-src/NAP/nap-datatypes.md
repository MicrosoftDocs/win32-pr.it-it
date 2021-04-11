---
title: Tipi di tipo di protezione accesso alla rete (NapTypes. h)
description: Nota la piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10 i tipi di dati per l'API di protezione accesso alla rete (NAP) sono i seguenti.
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
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
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964718"
---
# <a name="nap-datatypes"></a>Tipi di tipo di protezione accesso alla rete

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Di seguito sono riportati i tipi di dati per l'API di protezione accesso alla rete (NAP).


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

**ProbationTime**
</dt> <dd>

Struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che contiene un'ora relativa alla prova di un computer client.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Valore che specifica l'intervallo di valori possibili per la dimensione massima, in byte, di un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) definito dall'intervallo ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).

</dd> <dt>

**NapComponentId**
</dt> <dd>

Identificatore univoco a 4 byte utilizzato da SHAs, SHV e client di imposizione per identificarsi autonomamente. I primi tre byte sono il codice SMI assegnato dall'IETF del fornitore e l'ultimo byte identifica il componente stesso.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Valore **NapComponentId** utilizzato per identificare le coppie Sha/di convalida integrità.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Valore **NapComponentId** usato per identificare i client di imposizione.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Valore che specifica il numero di SHAs registrati nel sistema NAP nell'intervallo compreso tra 0 (zero) e [**maxSystemHealthEntityCount**](nap-type-constants.md).

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Valore che specifica il numero di client di imposizione nel sistema NAP nell'intervallo compreso tra 0 (zero) e [**maxEnforcerCount**](nap-type-constants.md).

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

Versione [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) di una struttura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) utilizzata per associare [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) a **SoHResponses**.

</dd> <dt>

**ConnectionId**
</dt> <dd>

Identificatore univoco globale (GUID) univoco utilizzato per identificare le connessioni NAP gestite dai client di imposizione.

</dd> <dt>

**Percentuale**
</dt> <dd>

Valore che contiene la percentuale compresa tra 0 (zero) e 100 di monitoraggio e aggiornamento completato

</dd> <dt>

**MessageId**
</dt> <dd>

Valore univoco utilizzato per identificare i messaggi di sistema NAP.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt> </dl> |



 

