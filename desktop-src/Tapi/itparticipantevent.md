---
description: L'interfaccia ITParticipantEvent contiene metodi che recuperano la descrizione degli eventi dei partecipanti.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interfaccia ITParticipantEvent (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f47e57bf1698a97be6811316409e596c9dfb03181e50b5f487798463c5cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864461"
---
# <a name="itparticipantevent-interface"></a>Interfaccia ITParticipantEvent

\[**ITParticipantEvent** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'interfaccia ITParticipantEvent** contiene metodi che recuperano la descrizione degli eventi dei partecipanti. Quando l'implementazione dell'applicazione del metodo [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica un EVENTO [**TAPI \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) uguale a **TE \_ PRIVATE,** il parametro *pEvent* del metodo è un **puntatore IDispatch** per l'interfaccia **ITParticipantEvent.** I metodi di questa interfaccia possono essere usati per recuperare informazioni relative a una modifica del partecipante che si è verificata.

> [!Note]  
> È necessario chiamare il [**metodo ITTAPI::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e impostare una maschera di filtro eventi che includa l'evento **TE \_ PRIVATE** per abilitare la ricezione degli eventi dei partecipanti. Se non si chiama **ITTAPI::p ut \_ EventFilter,** l'applicazione non riceverà eventi. Per altre informazioni, vedere Panoramica [degli](events.md) eventi.

 

## <a name="members"></a>Membri

**L'interfaccia ITParticipantEvent** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantEvent** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITParticipantEvent** include questi metodi.



| Metodo                                                         | Descrizione                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Evento \_ get**](itparticipantevent-get-event.md)             | Ottiene il [**descrittore \_ EVENTO PARTECIPANTE**](participant-event.md) dell'evento.<br/>                                                    |
| [**ottenere \_ un partecipante**](itparticipantevent-get-participant.md) | Ottiene un puntatore a una matrice [**di interfacce ITParticipant**](itparticipant.md) che rappresentano i partecipanti coinvolti nell'evento.<br/> |
| [**get \_ SubStream**](itparticipantevent-get-substream.md)     | Ottiene un puntatore a una matrice [**di interfacce ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) che rappresentano i sottostream coinvolti nell'evento.<br/>       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**EVENTO \_ PARTECIPANTE**](participant-event.md)
</dt> <dt>

[**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**EVENTO \_ TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Registrare il frammento di codice Events](register-events.md)
</dt> </dl>

 

