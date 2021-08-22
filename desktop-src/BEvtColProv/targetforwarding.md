---
description: Recupera i dati di inoltro da un computer di destinazione.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Classe TargetForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: a6025089d069504889d7b97d87a73b167746c3e594013acf58f0ed615162f787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529691"
---
# <a name="targetforwarding-class"></a>Classe TargetForwarding

Recupera i dati di inoltro da un computer di destinazione.

> [!Note]  
> In un computer di destinazione possono essere configurati più server d'inoltro.

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a>Members

La **classe TargetForwarding** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe TargetForwarding** ha queste proprietà.

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

 

