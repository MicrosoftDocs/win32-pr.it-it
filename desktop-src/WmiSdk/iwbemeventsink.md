---
description: Avvia la comunicazione con un provider di eventi utilizzando un set limitato di query.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interfaccia IWbemEventSink (Wbemprov. h)
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
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315994"
---
# <a name="iwbemeventsink-interface"></a>Interfaccia IWbemEventSink

L'interfaccia **IWbemEventSink** avvia la comunicazione con un provider di eventi usando un set di query limitato. Questa interfaccia estende [**IWbemObjectSink**](iwbemobjectsink.md), fornendo nuovi metodi di gestione della sicurezza e delle prestazioni. Per ulteriori informazioni sull'utilizzo di questa interfaccia, vedere la pagina relativa alla [scrittura di un provider di eventi](writing-an-event-provider.md) e alla [protezione degli eventi WMI](securing-wmi-events.md).

## <a name="members"></a>Membri

L'interfaccia **IWbemEventSink** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWbemEventSink** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Chiamato dall'utente per configurare le query di eventi con restrizioni.<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Controlla lo stato del sink di evento.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Chiamato dal consumer per impostare i parametri di invio in batch.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Utilizzato per aggiornare il descrittore di sicurezza in un sink di evento.<br/>   |



 

## <a name="remarks"></a>Commenti

Quando si implementa un sink di sottoscrizione di eventi ([**IWbemObjectSink**](iwbemobjectsink.md) o **IWbemEventSink**), non eseguire chiamate in WMI dall'interno dei metodi dell'oggetto sink. Ad esempio, la chiamata di [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) per annullare il sink dall'interno di un'implementazione di [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) può interferire con lo stato WMI. Per annullare una sottoscrizione di eventi, impostare un flag e chiamare **IWbemServices:: CancelAsyncCall** da un altro thread o oggetto. Per le implementazioni non correlate a un sink di evento, ad esempio il recupero di oggetti, enum e query, è possibile richiamarlo in WMI.

Le implementazioni di sink devono elaborare la notifica degli eventi entro 100 MSEC perché il thread WMI che recapita la notifica degli eventi non può eseguire altre operazioni finché l'oggetto sink non ha completato l'elaborazione. Se la notifica richiede una grande quantità di elaborazione, il sink può utilizzare una coda interna per gestire l'elaborazione da parte di un altro thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                            |
| Intestazione<br/>                   | <dl> <dt>Wbemprov. h (include Wbemidl. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API COM per WMI](com-api-for-wmi.md)
</dt> </dl>

 

 




