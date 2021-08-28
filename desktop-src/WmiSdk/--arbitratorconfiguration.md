---
description: Limita le risorse interne utilizzate dalle operazioni avviate dai client WMI.
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: __ArbitratorConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 4344eb368a96d2d47207748cba622d07d11ef78e0a046c6ea169305d9c587957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321121"
---
# <a name="__arbitratorconfiguration-class"></a>\_\_Classe ArbitratorConfiguration

La **\_ \_ classe ArbitratorConfiguration** è una classe di configurazione che limita le risorse interne usate dalle operazioni avviate dai client WMI. Si tratta di una classe singleton che risiede nello spazio \\ dei nomi radice. La classe viene generata internamente, quindi non è presente alcun file MOF.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a>Members

La **\_ \_ classe ArbitratorConfiguration** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe ArbitratorConfiguration** ha queste proprietà.

<dl> <dt>

**OutstandingTasksPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Numero di attività avviate dall'utente in sospeso contemporaneamente.

</dd> <dt>

**OutstandingTasksTotal**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Numero totale di attività in sospeso in qualsiasi momento.

</dd> <dt>

**PermanentSubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di sottoscrizioni permanenti consentite per un determinato utente contemporaneamente.

</dd> <dt>

**PermanentSubscriptionsTotal**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di sottoscrizioni permanenti consentite per tutti gli utenti contemporaneamente.

</dd> <dt>

**PollingInstructionsPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di query di eventi di polling consentite per un determinato utente contemporaneamente.

</dd> <dt>

**PollingInstructionsTotal**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di istruzioni di polling consentite per tutti gli utenti contemporaneamente.

</dd> <dt>

**PollingMemoryPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La quantità di query di eventi di polling della memoria, eseguite da un determinato utente, può essere utilizzata in qualsiasi momento.

</dd> <dt>

**PollingMemoryTotal**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Quantità totale di memoria che le query degli eventi di polling, per tutti gli utenti combinati, possono usare in qualsiasi momento.

</dd> <dt>

**QuotaRetryCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Numero di violazioni di quota consentite prima dell'annullamento di un'attività.

</dd> <dt>

**QuotaRetryWaitInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Ritardo introdotto nell'esecuzione dell'attività in ogni violazione di quota.

</dd> <dt>

**TaskThreadsPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Numero massimo di thread di attività associati a un determinato utente ogni volta.

</dd> <dt>

**TaskThreadsTotal**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Numero massimo di thread di attività.

</dd> <dt>

**TemporarySubscriptionsPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di sottoscrizioni temporanee consentite per un determinato utente contemporaneamente.

</dd> <dt>

**TemporarySubscriptionsTotal**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di sottoscrizioni temporanee consentite per tutti gli utenti contemporaneamente.

</dd> <dt>

**TotalCacheDisk**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Cache totale del disco associata a tutti gli utenti contemporaneamente.

</dd> <dt>

**TotalCacheDiskPerTask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Cache totale del disco associata a una determinata attività in qualsiasi momento.

</dd> <dt>

**TotalCacheDiskPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Cache totale del disco associata a un utente specifico in qualsiasi momento.

</dd> <dt>

**TotalCacheMemory**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Cache di memoria totale associata a tutti gli utenti contemporaneamente.

</dd> <dt>

**TotalCacheMemoryPerTask**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Cache di memoria totale associata a una determinata attività in qualsiasi momento.

</dd> <dt>

**TotalCacheMemoryPerUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Cache di memoria totale associata a un determinato utente in qualsiasi momento.

</dd> <dt>

**TotalUsers**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non utilizzato. Numero massimo di utenti connessi.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\_ \_ Il valore diConfiguration** viene ereditato da [**\_ \_ SystemClass.**](--systemclass.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Radice<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

