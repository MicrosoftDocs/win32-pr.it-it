---
description: Questo documento descrive le interfacce che forniscono metodi che consentono a un msp di interagire con l'ambiente Di telefonia Microsoft e di consentire a un'applicazione TAPI 3 di usare un controllo multimediale MSPs.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Informazioni di riferimento su Media Service Provider Interface (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94ce02312a7c94a7bc2b805a6c73c263546d9cb3f21bbe795d92a91b1010a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404751"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Informazioni di riferimento su Media Service Provider Interface (MSPI)

Questo documento illustra le interfacce che forniscono metodi che consentono a un msp di interagire con l'ambiente Di telefonia Microsoft e di consentire a un'applicazione TAPI 3 di usare i controlli multimediali di un provider di servizi multimediali.



| Interfacce dell'interfaccia del provider di servizi multimediali      | Descrizione                                                                                                                                                                            | Necessaria? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Esposto solo a TAPI. Interfaccia MSP principale per la DLL TAPI. TAPI 3 chiama **CoCreateInstance** su questa interfaccia per creare l'oggetto MSP.                                               | Sì       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di recuperare informazioni su un flusso, di avviarlo, sospenderlo o arrestarlo e di selezionare o deselezionare i terminali in un flusso. | Sì       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di creare o rimuovere flussi.                                                                                       | Sì       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Esposto alle applicazioni. Interfaccia dell'enumeratore [**per ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                                                                                        | Sì       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di recuperare informazioni su un flusso secondario, di avviarlo, sospenderlo o arrestarlo e di selezionare o deselezionare i terminali.          | Facoltativo  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di creare o rimuovere i sottostream.                                                                                    | Facoltativo  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Esposto alle applicazioni. Interfaccia dell'enumeratore [**per ITSubStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)                                                                                                  | Facoltativo  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Esposto alle applicazioni. Ottiene informazioni sull'oggetto [Terminal,](terminal-object.md)ad esempio chiamate terminali e supporti supportati.                                                    | Sì       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Esposto alle applicazioni. Fornisce metodi per eseguire query sui terminali disponibili e creare terminali aggiuntivi.                                                                             | Sì       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Esposto alle applicazioni. Recupera informazioni sulle classi terminali e sulle superclassi collegabili. deriva [**dall'interfaccia ITTerminalSupport.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)           | Sì       |



 

## <a name="media-service-provider-interface-types"></a>Tipi di interfaccia del provider di servizi multimediali

-   [**EVENTO \_ INDIRIZZO \_ MSP**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**EVENTO \_ DI CHIAMATA \_ MSP**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**EVENTO \_ MSP**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**INFORMAZIONI \_ \_ SULL'EVENTO MSP**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
