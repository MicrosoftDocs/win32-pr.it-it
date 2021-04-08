---
title: Rappresentazione dei dati
description: Gli ambienti di elaborazione possono variare in modo significativo, così come le architetture di rete.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- RPC (Remote Procedure Call), descrizione, rappresentazione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4de187f2b646e55cd4f1a269f0504a2d43e951c3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734538"
---
# <a name="data-representation"></a>Rappresentazione dei dati

Gli ambienti di elaborazione possono variare in modo significativo, così come le architetture di rete. Per soddisfare queste differenze, MIDL consente di modificare la modalità di rappresentazione dei dati. A volte è possibile semplificare lo sviluppo convertendo i dati in un formato che l'applicazione può gestire più facilmente. È possibile modificare il formato dei dati dell'applicazione in modo che possa essere trasmesso in modo più efficiente attraverso la rete.

Gli **\[** attributi [**trasmettono \_ come**](/windows/desktop/Midl/transmit-as) **\]** e **\[** [**rappresentano \_**](/windows/desktop/Midl/represent-as) gli **\]** attributi per indicare al compilatore di associare un tipo trasmissibile che lo stub passa tra il client e il server, con un tipo di utente utilizzato dalle applicazioni client e server. È necessario fornire le routine che eseguono la conversione tra il tipo di utente e il tipo trasmissibile e le routine per rilasciare la memoria utilizzata per contenere i dati convertiti. L'utilizzo dell'attributo **\[ trasmissione \_ come \]** IDL o dell'attributo **\[ rappresenta \_ come \]** ACF indica allo stub di chiamare queste routine di conversione prima e dopo la trasmissione. L' **\[** attributo [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) **\]** consente di convertire un tipo di dati in un altro tipo di dati per la trasmissione in rete. L' **\[** attributo [**rappresenta \_ come**](/windows/desktop/Midl/represent-as) **\]** consente di controllare il modo in cui i dati provenienti dalla rete vengono presentati all'applicazione.

Gli **\[** attributi [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) **\]** e **\[** [**User \_ Marshal**](/windows/desktop/Midl/user-marshal) **\]** sono estensioni Microsoft per l'IDL OSF-DCE. La sintassi e le funzionalità sono simili a quelle della trasmissione specificata da DCE **\[ \_ come \]** e **\[ rappresentano \_ rispettivamente \] come** attributi. La differenza consiste nel fatto che, anziché convertire i dati da un tipo a un altro, si effettua il marshalling dei dati direttamente. A tale scopo, è necessario fornire le routine esterne per dimensionare il buffer dei dati sui lati client e server, effettuare il marshalling e l'unmarshalling dei dati sul lato client e server e liberare i dati sul lato server. Il compilatore MIDL genera codici di formato che indicano al motore NDR di chiamare queste routine esterne quando necessario.

Gli attributi **\[ Wire \_ Marshal \]** e **\[ User \_ Marshal \]** consentono di effettuare il marshalling dei tipi di dati che altrimenti non potevano essere trasmessi attraverso i limiti del processo. Inoltre, poiché è presente un sovraccarico minore associato alla conversione del tipo, il **\[ \_ \] marshalling di rete** e il **\[ \_ marshalling \] dell'utente** forniscono prestazioni migliori in fase di esecuzione, se confrontato con la **\[ trasmissione \_ come \]** e **\[ rappresentano \_ come \]**. Gli attributi **di marshalling e di \[ marshalling \_ degli utenti si escludono reciprocamente tra loro e per quanto riguarda la trasmissione come e rappresentano gli attributi per un tipo specificato. \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]**

È importante notare che l'implementazione del **\[ \_ marshalling \] di Wire** e degli attributi di **\[ \_ marshalling \] degli utenti** deve seguire le regole di marshalling stabilite dalla specifica OSF-DCE. Per questo motivo, non è consigliabile usare questi attributi se non si ha familiarità con il protocollo wire. Altre informazioni relative al trasferimento della sintassi NDR sono reperibili in [www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

Questa sezione fornisce una breve panoramica di questi attributi MIDL negli argomenti seguenti:

-   [**Trasmettere \_ come e rappresentare \_ gli attributi**](the-transmit-as-and-represent-as-attributes.md)
-   [**\_Attributi di marshalling di rete e di \_ marshalling degli utenti**](the-wire-marshal-and-user-marshal-attributes.md)

 

 