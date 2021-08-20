---
description: Il processo di registrazione degli eventi avviene quando il terminale viene selezionato da un flusso.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrazione per gli eventi del terminale collegabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71993d597cbcba7c634068813eb14939539dc7e7d43cda0105e8cf9ee615a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060459"
---
# <a name="registering-for-pluggable-terminal-events"></a>Registrazione per gli eventi del terminale collegabile

Il processo di registrazione degli eventi avviene quando il terminale viene selezionato da un flusso. Nell'implementazione del metodo [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) dell'applicazione terminale è possibile usare l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) del terminale collegato al flusso e chiamare **QueryInterface** per trovare [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Se la **chiamata QueryInterface** ha esito positivo, è possibile chiamare il [**metodo RegisterSink.**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) A questo scopo, è necessario creare un oggetto che implementa [**l'interfaccia ITPluggableTerminalEventSink.**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) Questa interfaccia viene passata come parametro del **metodo RegisterSink.**

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

Il terminale che implementa [**la chiamata ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) archivierà l'interfaccia . Il puntatore verrà usato quando il terminale genererà un evento.

È possibile annullare la registrazione del sink di evento [**usando UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
