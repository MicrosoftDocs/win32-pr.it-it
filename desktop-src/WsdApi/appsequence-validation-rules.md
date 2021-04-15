---
description: AppSequence informazioni contenute in WS-Discovery messaggi di annuncio e risposta (Hello, ProbeMatches e ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Regole di convalida AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528591"
---
# <a name="appsequence-validation-rules"></a>Regole di convalida AppSequence

AppSequence informazioni contenute in WS-Discovery messaggi di annuncio e risposta ([Hello](hello-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md)). Queste informazioni vengono elaborate e convalidate da WSDAPI prima che questi messaggi vengano passati ai componenti sopra lo stack, ad esempio Network Explorer o un'applicazione che chiama WSDAPI.

Nel codice XML seguente viene illustrato un elemento AppSequence di esempio. Il prefisso WSD si riferisce allo spazio dei nomi `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI ignora i messaggi non aggiornati. Per ogni dispositivo (identificato in modo univoco dall'indirizzo endpoint nel corpo SOAP), WSDAPI ignora tutti i messaggi con un MessageNumber AppSequence inferiore rispetto all'ultimo messaggio visualizzato.

WSDAPI ignora gli annunci XAddr non aggiornati. Se AppSequence InstanceId è inferiore rispetto all'ultimo InstanceId rilevato, WSDAPI ignora la XAddrs annunciata nel corpo SOAP. Se, inoltre, InstanceId è uguale al precedente, ma il valore di MetadataVersion è inferiore rispetto all'ultimo MetadataVersion, WSDAPI ignora il XAddrs.

WSDAPI ignora i messaggi di WS-Discovery duplicati. Se a WSDAPI vengono inviati due messaggi di WS-Discovery identici, verranno elaborati solo i primi messaggi ricevuti. Questo è in genere rilevante solo per le applicazioni che effettuano chiamate direttamente nelle interfacce [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) o [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



