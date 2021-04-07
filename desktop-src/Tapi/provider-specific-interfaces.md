---
description: TAPI 3 supporta l'integrazione di interfacce specifiche del provider di servizi negli oggetti standard, consentendo alle applicazioni di sfruttare le funzionalità specifiche del provider.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfacce di Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058060"
---
# <a name="provider-specific-interfaces"></a>Interfacce di Provider-Specific

TAPI 3 supporta l'integrazione di interfacce specifiche del provider di servizi negli oggetti standard, consentendo alle applicazioni di sfruttare le funzionalità specifiche del provider. Inoltre, TAPI 3 consente ai provider di servizi di fornire eventi specifici del fornitore alle applicazioni come oggetti COM sulla stessa interfaccia in cui l'applicazione riceve gli eventi standard.

TAPI realizza questa integrazione aggregando oggetti specifici del provider con gli oggetti standard, ovvero TAPI, Address, Terminal, Call e CallHub, e inviando o delegando metodi sconosciuti a questi oggetti specifici del provider.

Un provider di servizi, ad esempio, può consentire alle applicazioni di ottenere informazioni su una chiamata oltre a quelle esposte dall'interfaccia [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) . Il fornitore deve definire un'interfaccia che consente alle applicazioni di eseguire queste query aggiuntive e di implementare tale interfaccia in un oggetto. Questo oggetto implementa anche un'interfaccia di query sul fornitore, in modo che un'applicazione possa individuare quali tipi di funzioni specifiche del provider potrebbero essere disponibili.

Quando l'applicazione ottiene un riferimento a un oggetto chiamata, l'applicazione può usare la nuova interfaccia specifica del provider e i relativi metodi come se fossero implementati dall'oggetto chiamata stesso.

Per un elenco di tutte le interfacce MSP standard, vedere informazioni di [riferimento sull'interfaccia del provider di servizi multimediali (MSPI)](media-service-provider-interface-mspi-reference.md) .

Vedere [IPConf msp Interfaces](ipconf-msp-interfaces.md) per un elenco di tutte le interfacce specifiche di IPConf msp.

 

 



