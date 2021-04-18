---
description: L'interfaccia ITParticipantEvent contiene metodi che recuperano la descrizione degli eventi del partecipante.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interfaccia ITParticipantEvent (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328728"
---
# <a name="itparticipantevent-interface"></a>Interfaccia ITParticipantEvent

\[**ITParticipantEvent** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITParticipantEvent** contiene metodi che recuperano la descrizione degli eventi del partecipante. Quando l'implementazione dell'applicazione del metodo [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica un [**\_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) uguale a **te \_ private**, il parametro *pEvent* del metodo è un puntatore **IDispatch** per l'interfaccia **ITParticipantEvent** . I metodi di questa interfaccia possono essere utilizzati per recuperare le informazioni relative a una modifica del partecipante che si è verificata.

> [!Note]  
> È necessario chiamare il metodo [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e impostare una maschera di filtro eventi che includa l'evento **\_ privato te** per abilitare la ricezione degli eventi del partecipante. Se non si chiama **ITTAPI::p UT \_ EventFilter**, l'applicazione non riceverà alcun evento. Per ulteriori informazioni, vedere Cenni preliminari [sugli eventi](events.md) .

 

## <a name="members"></a>Membri

L'interfaccia **ITParticipantEvent** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantEvent** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITParticipantEvent** dispone di questi metodi.



| Metodo                                                         | Descrizione                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ottieni \_ evento**](itparticipantevent-get-event.md)             | Ottiene il descrittore di [**\_ eventi del partecipante**](participant-event.md) dell'evento.<br/>                                                    |
| [**Ottieni \_ partecipante**](itparticipantevent-get-participant.md) | Ottiene un puntatore a una matrice di interfacce [**ITParticipant**](itparticipant.md) che rappresentano i partecipanti coinvolti nell'evento.<br/> |
| [**ottenere il \_ Sottoflusso**](itparticipantevent-get-substream.md)     | Ottiene un puntatore a una matrice di interfacce [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) che rappresentano i flussi sottoflussi necessari nell'evento.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**\_evento partecipante**](participant-event.md)
</dt> <dt>

[**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**\_evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Frammento di codice eventi di registrazione](register-events.md)
</dt> </dl>

 

