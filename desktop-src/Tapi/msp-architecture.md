---
description: Nell'architettura TAPI tutti i TSPs vengono eseguiti nel contesto di TAPISRV, che viene implementato come un processo del servizio all'interno di SVCHOST.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: Architettura MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c1229ddce90f79c122c47572b4567d230b0b4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401566"
---
# <a name="msp-architecture"></a>Architettura MSP

Nell'architettura TAPI tutti i TSPs vengono eseguiti nel contesto di TAPISRV, che viene implementato come un processo del servizio all'interno di SVCHOST. Le applicazioni TAPI si trovano in un processo. Le applicazioni TAPI caricano Tapi3.dll e tutte le MSPs necessarie nel proprio processo e la DLL TAPI comunica con TAPISRV tramite un'interfaccia RPC privata. Il diagramma seguente illustra l'interazione di questi componenti.

![interazioni tra tapisrv, applicazioni TAPI e Msps](images/tsp-msp1.png)

Un provider di servizi multimediali (MSP) fornisce flussi multimediali usando le astrazioni di terminali, flussi e sottoflussi.

Un terminale è un sink o un'origine per un flusso multimediale. Potrebbe trattarsi di un oggetto fisico, ad esempio un altoparlante o un microfono, oppure un'astrazione di un dispositivo, ad esempio una finestra video. L' [oggetto terminale](terminal-object.md) espone l'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . La classe del terminale è descritta dal GUID della [**classe terminale**](terminal-class.md) . Un MSP può definire le proprie classi terminal.

I flussi dividono il supporto di una chiamata in base al tipo o al tipo di [**supporto**](tapimediatype--constants.md) , alla [**direzione**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)del flusso e all'indirizzo di destinazione del supporto. Ad esempio, un flusso audio in ingresso da un modem è un oggetto flusso, un flusso video in uscita a un indirizzo IP e una porta è un oggetto flusso, i flussi video provenienti da un gruppo multicast IP vengono considerati anche come un unico oggetto flusso. L'oggetto Stream è rappresentato dall'interfaccia [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) .

I sottoflussi consentono un controllo più preciso sui supporti. Nel caso del multicast IP, ad esempio, l'oggetto flusso video in entrata potrebbe rappresentare più persone. È probabile che l'applicazione disponga di un renderer separato per ogni partecipante. Il flusso video in ingresso può essere suddiviso in più flussi, uno per ogni persona. Un sottoflusso corrisponderebbe a una persona e può essere configurato e controllato separatamente. L'oggetto substream è rappresentato dall'interfaccia [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) .

Quando un'applicazione chiama [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) per impostare una chiamata, deve specificare il tipo di supporto richiesto. In una chiamata in uscita, indica semplicemente TAPI quando viene creata la chiamata. Ad esempio:

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

I tipi di supporto passati indicano i supporti a cui l'applicazione è interessata per la durata della chiamata. Ad esempio, l'applicazione può specificare audio e video durante la creazione della chiamata, ma selezionare solo terminali audio all'inizio. Il file MSP avvierà solo il flusso audio, ma non rifiuterà una richiesta video locale o remota effettuata successivamente nel corso della chiamata.

Quando l'applicazione chiama [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), TAPI 3 chiama [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) nel TSP. Dopo che è stata stabilita una chiamata, MSP e TSP possono comunicare secondo necessità.

Quando si esegue la disconnessione di una chiamata, è necessario che l'MSP e il TSP comunicano in caso di interruzione della chiamata. Tapi3.dll chiamerà [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) se l'applicazione chiama [**Disconnetti**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
