---
description: Nell'architettura TAPI tutti i TSP vengono eseguiti nel contesto di TAPISRV, implementato come processo del servizio all'interno di SVCHOST.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: Architettura MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cf5d95cf568e17b53c575f6c2f8963baa4b698cc69243ee1a23e9306ad6b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002849"
---
# <a name="msp-architecture"></a>Architettura MSP

Nell'architettura TAPI tutti i TSP vengono eseguiti nel contesto di TAPISRV, implementato come processo del servizio all'interno di SVCHOST. Le applicazioni TAPI sono in esecuzione nel proprio processo. Le applicazioni TAPI Tapi3.dll e gli eventuali MSP necessari nel proprio processo e la DLL TAPI comunica con TAPISRV tramite un'interfaccia RPC privata. Il diagramma seguente illustra l'interazione di questi componenti.

![interazioni tra tapisrv, applicazioni Tapi e msp](images/tsp-msp1.png)

Un provider di servizi multimediali (MSP) fornisce lo streaming multimediale usando le astrazioni di terminali, Flussi e substream.

Un terminale è un sink o un'origine per un flusso multimediale. Può essere un oggetto fisico, ad esempio un altoparlante o un microfono, oppure un'astrazione di un dispositivo, ad esempio una finestra video. [L'oggetto terminale](terminal-object.md) espone [**l'interfaccia ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) La classe del terminale è descritta dal GUID [**della classe terminale.**](terminal-class.md) Un msp può definire le proprie classi terminali.

Flussi dividere il supporto di una chiamata [](tapimediatype--constants.md) in base al tipo [](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)o al tipo di supporto, alla direzione del flusso e all'indirizzo di destinazione del supporto. Ad esempio, un flusso audio in ingresso da un modem è un oggetto flusso, un flusso video in uscita a un indirizzo IP e la porta è un oggetto flusso, i flussi video provenienti da un gruppo multicast IP vengono considerati anche come un oggetto flusso. L'oggetto Stream è rappresentato [**dall'interfaccia ITStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)

I sottostream consentono un controllo più fine sui supporti. Ad esempio, nel caso del multicast IP, l'oggetto flusso video in ingresso potrebbe rappresentare diverse persone. È probabile che l'applicazione voglia che ogni partecipante abbia un renderer separato. Il flusso video in ingresso può essere suddiviso in diversi sottostream, uno per ogni persona. Un flusso secondario corrisponde a una persona e può essere configurato e controllato separatamente. L'oggetto SubStream è rappresentato [**dall'interfaccia ITSubStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol)

Quando un'applicazione [**chiama ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) per configurare una chiamata, deve specificare il tipo di supporto necessario. In una chiamata in uscita, indica semplicemente a TAPI quando viene creata la chiamata. Esempio:

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

In questo caso, l'applicazione sta creando una chiamata audio-video in uscita.

I tipi di supporti passati in indicano il supporto a cui l'applicazione è interessata per tutta la durata della chiamata. Ad esempio, l'applicazione può specificare audio e video durante la creazione della chiamata, ma selezionare solo terminali audio all'inizio. Il msp inizierà a trasmettere solo l'audio, ma non rifiuterà una richiesta video locale o remota effettuata in un secondo momento nel corso della chiamata.

Quando l'applicazione chiama [**quindi ITBasicCallControl::Connessione**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), TAPI 3 chiama [**\_ lineMakeCall TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) nel TSP. Dopo aver stabilito una chiamata, msp e TSP possono comunicare in base alle esigenze.

Quando una chiamata si disconnette, il provider di servizi di configurazione e il provider di servizi di configurazione comunicano la rimozione della chiamata. Tapi3.dll chiama [**\_ lineDrop TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) se l'applicazione chiama [**Disconnect.**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)

 

 
