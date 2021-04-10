---
description: Consente di impostare i limiti nell'utilizzo del processo host delle risorse di sistema.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: Classe __ProviderHostQuotaConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231827"
---
# <a name="__providerhostquotaconfiguration-class"></a>\_\_Classe ProviderHostQuotaConfiguration

La classe di sistema **\_ \_ ProviderHostQuotaConfiguration** è una classe di configurazione per i processi del provider host. Questa classe risiede nello spazio dei nomi radice e consente di impostare i limiti nell'utilizzo del processo host delle risorse di sistema.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a>Members

La classe **\_ \_ ProviderHostQuotaConfiguration** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ ProviderHostQuotaConfiguration** dispone di queste proprietà.

<dl> <dt>

**HandlesPerHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Numero di handle di oggetti kernel che possono essere presenti in ogni host.

</dd> <dt>

**MemoryAllHosts**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Quantità combinata di memoria privata in byte che può essere utilizzata da tutti gli host.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MemoryPerHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Quantità di memoria privata che può essere mantenuta da ogni host.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ProcessLimitAllHosts**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Numero totale di processi host che possono essere eseguiti contemporaneamente.

</dd> <dt>

**ThreadsPerHost**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Numero di thread di proprietà di un host.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le proprietà che rappresentano i limiti possono essere modificate, ma poiché la classe è un singleton, tutti gli host del provider condividono gli stessi limiti.

Quando si configurano i limiti per l'oggetto processo host, vengono utilizzati i parametri seguenti:

-   **MemoryAllHosts**
-   **MemoryPerHost**
-   **ProcessLimitAllHosts**
-   **ThreadsPerHost**

Il processo host esegue il polling dell'utilizzo e chiude il processo se la quota **HandlesPerHost** viene violata. Le modifiche apportate a questi valori diventano effettive dopo il riavvio del computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

