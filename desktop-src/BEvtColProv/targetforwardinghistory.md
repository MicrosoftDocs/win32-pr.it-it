---
description: Cronologia recente delle modifiche ai dati di inoltro per un computer di destinazione.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Classe TargetForwardingHistory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: a58168995adf81f01d20486bcb7ceeef85b9424b2034da98ef628e098a674f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529641"
---
# <a name="targetforwardinghistory-class"></a>Classe TargetForwardingHistory

Cronologia recente delle modifiche ai dati di inoltro per un computer di destinazione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a>Members

La **classe TargetForwardingHistory** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe TargetForwardingHistory** ha queste proprietà.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Informazioni sull'endpoint del server dell'agente di raccolta. Questa proprietà è formattata come *host*:*stringa di* porta.

</dd> <dt>

**Computer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome computer del computer di destinazione.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp che indica quando è stata stabilita la connessione per i dati di inoltro.

</dd> <dt>

**Destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Destinazione dei dati di inoltro, ad esempio un nome file.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Formato utilizzato per generare la destinazione dei dati di inoltro.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp che indica quando la connessione è stata disconnessa.

</dd> <dt>

**Error (Errore) (Error (Errore)e)**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Messaggio di errore che descrive un errore rilevato. Questa proprietà è vuota se non si è verificato alcun errore.

</dd> <dt>

**Tipo di server d'inoltro**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Tipo di file che contiene i dati di inoltro, ad esempio ETL.

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Informazioni sull'endpoint del computer di destinazione, in formato leggibile dall'utente. Questa proprietà è formattata come *host*:*stringa di* porta. Ad esempio, "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

GUID SMBIOS **del** computer di destinazione.

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Indirizzo MAC del computer di destinazione.

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp di quando è stata registrata la modifica dello stato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider WMI dell'agente di raccolta eventi di avvio](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

