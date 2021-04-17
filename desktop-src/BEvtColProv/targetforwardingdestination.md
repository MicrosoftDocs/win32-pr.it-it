---
description: Destinazioni note che contengono i dati raccolti. Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Classe TargetForwardingDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482796"
---
# <a name="targetforwardingdestination-class"></a>Classe TargetForwardingDestination

Destinazioni note che contengono i dati raccolti. Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

La classe **TargetForwardingDestination** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **TargetForwardingDestination** dispone di queste proprietà.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Host: informazioni sulla porta dell'endpoint sul lato agente di raccolta.

</dd> <dt>

**Computer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome del computer di destinazione, come determinato dall'agente di raccolta in base alla relativa configurazione.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp del momento in cui è stata stabilita la connessione.

</dd> <dt>

**Destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Destinazione dei dati. Il significato dipende dal tipo di server d'avanzamento. Può essere un nome di file o un'altra identificazione.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Modello utilizzato per generare la destinazione dei dati. Il significato dipende dal tipo e dalla configurazione del server d'avanzamento. Per una destinazione fissa, sarà uguale alla destinazione stessa. Per la destinazione con rotazione dei file sono inclusi i caratteri di pattern che verranno sostituiti con l'indice effettivo nella destinazione.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp del momento in cui la connessione è stata eliminata.

</dd> <dt>

**Error (Errore) (Error (Errore)e)**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Messaggio di errore se si è verificato un errore. In caso contrario, sarà vuoto.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Tipo del server d'inoltre (ad esempio "ETL").

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Informazioni sull'endpoint del computer di destinazione, in formato leggibile. Questa proprietà è formattata come stringa *host*:*porta* . Ad esempio, "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Il GUID SMBIOS del computer di destinazione (se noto).

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Indirizzo MAC del computer di destinazione (se noto).

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp di quando è stata registrata questa modifica dello stato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Radice \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

