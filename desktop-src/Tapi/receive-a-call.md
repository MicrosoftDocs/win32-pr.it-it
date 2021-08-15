---
description: Nell'esempio di codice seguente viene illustrata la gestione delle nuove notifiche di chiamata, ad esempio la ricerca o la creazione di terminali appropriati per il rendering del contenuto multimediale.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Ricevere una chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e4ce02ec11a1373d16b9b9ebd0fba29313b1d532175894c6fd1b12a38e2bf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060469"
---
# <a name="receive-a-call"></a>Ricevere una chiamata

Nell'esempio di codice seguente viene illustrata la gestione delle nuove notifiche di chiamata, ad esempio la ricerca o la creazione di terminali appropriati per il rendering del contenuto multimediale. Questo esempio è una parte dell'istruzione switch che un'applicazione deve implementare per la gestione degli eventi. Il codice stesso può essere contenuto nell'implementazione di [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)oppure il metodo **Event** può inviare un messaggio a un thread di lavoro che contiene l'opzione .

Prima di usare questo esempio di codice, è necessario eseguire le operazioni in [Inizializza TAPI,](initialize-tapi.md) [Selezionare un indirizzo](select-an-address.md)e [Registrare eventi](register-events.md).

È inoltre necessario eseguire le operazioni illustrate in Selezionare un [terminale](select-a-terminal.md) dopo il recupero dei puntatori all'interfaccia [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) [**e ITAddress.**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)

> [!Note]  
> In questo esempio non sono disponibili il controllo degli errori e le versioni appropriate per il codice di produzione.

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Eventi](events.md)
</dt> <dt>

[**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
