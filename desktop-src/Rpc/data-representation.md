---
title: Rappresentazione dei dati
description: Gli ambienti di elaborazione possono differire in modo significativo, così come le architetture di rete.
ms.assetid: 34ba76ae-644d-4168-886f-0909a65f1abd
keywords:
- RPC Remote Procedure Call, descritta, rappresentazione dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9a0af96249c356f171396eaf52f91c5e33005eda080929cfbd8eecde27ffa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022091"
---
# <a name="data-representation"></a>Rappresentazione dei dati

Gli ambienti di elaborazione possono differire in modo significativo, così come le architetture di rete. Per soddisfare queste differenze, MIDL consente di modificare la modalità di rappresentazione dei dati. A volte è possibile semplificare lo sviluppo convertendo i dati in un formato che l'applicazione può gestire più facilmente. È possibile modificare il formato dei dati dell'applicazione in modo che possa essere trasmesso in modo più efficiente in rete.

La **\[** [**\_ trasmissione come**](/windows/desktop/Midl/transmit-as) e rappresentano come attributi indica al compilatore di associare un tipo trasmissibile che lo stub passa tra client e server, con un tipo di utente utilizzato dalle applicazioni client e **\]** **\[** [**\_**](/windows/desktop/Midl/represent-as) **\]** server. È necessario fornire le routine che eservino la conversione tra il tipo utente e il tipo trasmissibile e le routine per rilasciare la memoria utilizzata per contenere i dati convertiti. **\[ L'uso \_ \] dell'attributo transmit come** IDL o di **\[ rappresenta \_ \]** come attributo ACF indica al stub di chiamare queste routine di conversione prima e dopo la trasmissione. **\[** [**L'attributo transmit \_ as**](/windows/desktop/Midl/transmit-as) **\]** consente di convertire un tipo di dati in un altro tipo di dati per la trasmissione in rete. **\[** [**L'attributo represent \_ as**](/windows/desktop/Midl/represent-as) consente di controllare il modo in cui i **\]** dati della rete vengono presentati all'applicazione.

Gli **\[** [**attributi wire \_ marshal**](/windows/desktop/Midl/wire-marshal) **\]** e user **\[** [**\_ marshal**](/windows/desktop/Midl/user-marshal) **\]** sono estensioni Microsoft dell'IDL OSF-DCE. La sintassi e la funzionalità sono simili a quelle della trasmissione specificata da DCE **\[ \_ rispettivamente \]** **\[ \_ \]** come e rappresentano come attributi. La differenza è che, invece di convertire i dati da un tipo a un altro, si effettua direttamente il marshalling dei dati. A tale scopo, è necessario fornire le routine esterne per ridimensionare il buffer di dati sul lato client e server, effettuare il marshalling e l'unmarsshaling dei dati sul lato client e server e liberare i dati sul lato server. Il compilatore MIDL genera codici di formato che indica al motore NDR di chiamare queste routine esterne quando necessario.

Gli **\[ attributi wire \_ marshal \]** **\[ e user \_ marshal \]** rendono possibile il marshalling di tipi di dati che altrimenti non potevano essere trasmessi attraverso i limiti del processo. Inoltre, poiché alla conversione del tipo è associato un sovraccarico minore, il **\[ wire \_ marshal \]** e il **\[ \_ marshalling \]** dell'utente offrono prestazioni migliori in fase di esecuzione, **\[ \_ \]** rispetto alla trasmissione come e rappresentano **\[ \_ come \]**. Gli **\[ attributi wire \_ \] marshal** e **\[ user \_ marshal \]** **\[ \_ \]** si escludono reciprocamente l'uno rispetto all'altro e rispetto alla trasmissione come e rappresentano **\[ \_ \] come** attributi per un determinato tipo.

È importante notare che l'implementazione degli attributi **\[ wire \_ marshal \]** e **\[ user \_ marshal \]** deve seguire le regole di marshalling dettate dalla specifica OSF-DCE. Per questo motivo, l'uso di questi attributi non è consigliato se non si ha familiarità con il protocollo di collegamento. Altre informazioni sul trasferimento della sintassi NDR sono disponibili in [www.opengroup.org](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).

In questa sezione viene fornita una breve panoramica degli attributi MIDL negli argomenti seguenti:

-   [**La \_ trasmissione come e rappresentano \_ come attributi**](the-transmit-as-and-represent-as-attributes.md)
-   [**Attributi wire \_ marshal e user \_ marshal**](the-wire-marshal-and-user-marshal-attributes.md)

 

 