---
description: Destinazioni note contenenti i dati raccolti. Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.
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
ms.openlocfilehash: 58492b8b334085a6dd03c397558c4f10bc1fa4aff441f5b7bbfc7ba7cf37b0bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589001"
---
# <a name="targetforwardingdestination-class"></a>Classe TargetForwardingDestination

Destinazioni note contenenti i dati raccolti. Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.

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

La **classe TargetForwardingDestination** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe TargetForwardingDestination** ha queste proprietà.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Informazioni host:porta dell'endpoint sul lato dell'agente di raccolta.

</dd> <dt>

**Computer**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome del computer di destinazione, come determinato dall'agente di raccolta in base alla relativa configurazione.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp del momento in cui è stata stabilita la connessione.

</dd> <dt>

**Destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Destinazione dei dati. Il significato dipende dal tipo di server d'inoltro. Può essere un nome file o un'altra identificazione.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Modello usato per generare la destinazione dei dati. Il significato dipende dal tipo di server d'inoltro e dalla configurazione. Per una destinazione fissa, sarebbe uguale alla destinazione stessa. Per la destinazione con rotazione dei file conterrebbe i caratteri di criterio che verranno sostituiti con l'indice effettivo nella destinazione.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp dell'ora in cui è stata eliminata la connessione.

</dd> <dt>

**Error (Errore) (Error (Errore)e)**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Messaggio di errore se si è verificato un errore. In caso contrario, sarà vuoto.

</dd> <dt>

**Tipo di server d'inoltro**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](/windows/desktop/WmiSdk/key-qualifier) [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Tipo del server d'inoltro,ad esempio "etl".

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Informazioni sull'endpoint del computer di destinazione, in formato leggibile. Questa proprietà è formattata come *stringa di**porta* host: . Ad esempio, "127.0.0.1:50000".

</dd> <dt>

**Guida di destinazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

GUID SMBIOS del computer di destinazione (se noto).

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Indirizzo MAC del computer di destinazione (se noto).

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **fissi**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Timestamp del momento in cui è stata registrata la modifica dello stato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

