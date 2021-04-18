---
description: In questo documento vengono descritte le interfacce che forniscono metodi che consentono a un MSP di interagire con l'ambiente di telefonia Microsoft e consentono a un'applicazione TAPI 3 di usare i controlli MSPs.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Guida di riferimento all'interfaccia MSPI (Media Service Provider Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30b961fff4d8a9e50fb35573633cc2dc06e370c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320654"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Guida di riferimento all'interfaccia MSPI (Media Service Provider Interface)

Questo documento illustra le interfacce che forniscono metodi che consentono a un MSP di interagire con l'ambiente di telefonia Microsoft e consentono a un'applicazione TAPI 3 di usare i controlli multimediali di un MSP.



| Interfacce dell'interfaccia del provider di servizi multimediali      | Descrizione                                                                                                                                                                            | Necessaria? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Esposto solo a TAPI. Interfaccia MSP principale per la DLL TAPI. TAPI 3 chiama **CoCreateInstance** su questa interfaccia per creare l'oggetto msp.                                               | Sì       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di recuperare informazioni su un flusso, di avviarlo, sospenderlo o arrestarlo, nonché di selezionare o deselezionare i terminali in un flusso. | Sì       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di creare o rimuovere flussi.                                                                                       | Sì       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Esposto alle applicazioni. Interfaccia enumeratore per [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).                                                                                                        | Sì       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di recuperare informazioni su un sottoflusso, di avviarlo, sospenderlo o arrestarlo, nonché di selezionare o deselezionare i terminali.          | Facoltativo  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Esposto alle applicazioni. Fornisce metodi che consentono a un'applicazione di creare o rimuovere sottoflussi.                                                                                    | Facoltativo  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Esposto alle applicazioni. Interfaccia enumeratore per [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream).                                                                                                  | Facoltativo  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Esposto alle applicazioni. Ottiene informazioni sull' [oggetto terminale](terminal-object.md), ad esempio la chiamata Terminal e i supporti supportati.                                                    | Sì       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Esposto alle applicazioni. Fornisce metodi per eseguire query sui terminali disponibili e creare terminali aggiuntivi.                                                                             | Sì       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Esposto alle applicazioni. Recupera le informazioni sulle classi e le superclassi terminali di collegamento. deriva dall'interfaccia [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) .           | Sì       |



 

## <a name="media-service-provider-interface-types"></a>Tipi di interfaccia del provider di servizi multimediali

-   [**\_evento di indirizzo msp \_**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**\_evento chiamata \_ msp**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**\_evento msp**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**\_informazioni evento \_ msp**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia del provider di servizi multimediali (MSPI)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
