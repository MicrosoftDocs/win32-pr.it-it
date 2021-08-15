---
description: Avvia la comunicazione con un provider di eventi usando un set di query con restrizioni.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interfaccia IWbemEventSink (Wbemprov.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 10c5fa56a96db3e46ce2c4c7941fd7a1d6fb27a1730dc3741890935782e4ace7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318097"
---
# <a name="iwbemeventsink-interface"></a>Interfaccia IWbemEventSink

**L'interfaccia IWbemEventSink** avvia la comunicazione con un provider di eventi usando un set limitato di query. Questa interfaccia estende [**IWbemObjectSink,**](iwbemobjectsink.md)fornendo nuovi metodi che gestiscono sicurezza e prestazioni. Per altre informazioni sull'uso di questa interfaccia, vedere [Scrittura di un provider di eventi](writing-an-event-provider.md) e Protezione di eventi [WMI.](securing-wmi-events.md)

## <a name="members"></a>Membri

**L'interfaccia IWbemEventSink** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWbemEventSink** include questi metodi.



| Metodo                                                                | Descrizione                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Chiamato dal consumer per configurare query di eventi con restrizioni.<br/> |
| [**Isactive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Controlla lo stato del sink di evento.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Chiamato dal consumer per impostare i parametri di invio in batch.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Usato per aggiornare il descrittore di sicurezza in un sink di evento.<br/>   |



 

## <a name="remarks"></a>Commenti

Quando si implementa un sink di sottoscrizione di eventi ([**IWbemObjectSink**](iwbemobjectsink.md) o **IWbemEventSink**), non chiamare in WMI dall'interno dei metodi nell'oggetto sink. Ad esempio, la chiamata [**a IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) per annullare il sink dall'interno di un'implementazione di [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) può interferire con lo stato WMI. Per annullare una sottoscrizione di eventi, impostare un flag e chiamare **IWbemServices::CancelAsyncCall** da un altro thread o oggetto. Per le implementazioni non correlate a un sink di evento, ad esempio il recupero di oggetti, enumerazioni e query, è possibile richiamare WMI.

Le implementazioni del sink devono elaborare la notifica degli eventi entro 100 MSEC perché il thread WMI che recapita la notifica degli eventi non può eseguire altre operazioni fino al completamento dell'elaborazione dell'oggetto sink. Se la notifica richiede una grande quantità di elaborazione, il sink può usare una coda interna per un altro thread per gestire l'elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                            |
| Intestazione<br/>                   | <dl> <dt>Wbemprov.h (includere Wbemidl.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Wbemuuid.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API COM per WMI](com-api-for-wmi.md)
</dt> </dl>

 

 




