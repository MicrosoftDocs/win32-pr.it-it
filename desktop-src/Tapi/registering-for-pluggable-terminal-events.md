---
description: Il processo di registrazione dell'evento viene eseguito quando il terminale viene selezionato da un flusso.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrazione per eventi Terminal collegabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885826"
---
# <a name="registering-for-pluggable-terminal-events"></a>Registrazione per eventi Terminal collegabili

Il processo di registrazione dell'evento viene eseguito quando il terminale viene selezionato da un flusso. Nell'implementazione dell'applicazione terminal del metodo [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) , è possibile usare l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) del terminale collegato al flusso e chiamare **QueryInterface** per trovare [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Se la chiamata **QueryInterface** ha esito positivo, è possibile chiamare il metodo [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) . A questo scopo, è necessario creare un oggetto che implementi l'interfaccia [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) . Questa interfaccia viene passata come parametro del metodo **RegisterSink** .

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

Il terminale che implementa la chiamata [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) archivia l'interfaccia. Il puntatore verrà usato quando il terminale genererà un evento.

Il sink di evento può essere annullato tramite [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
