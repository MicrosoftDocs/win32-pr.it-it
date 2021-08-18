---
description: Informazioni appSequence contenute WS-Discovery messaggi di annuncio e risposta (Hello, ProbeMatches e ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Regole di convalida appSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f2acec9d9d3858b5d68b0240499d95dba059ac1bcac745f1dc69bebc2056a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738644"
---
# <a name="appsequence-validation-rules"></a>Regole di convalida appSequence

Informazioni appSequence contenute WS-Discovery messaggi di annuncio e risposta ([Hello](hello-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md)). Queste informazioni vengono elaborate e convalidate da WSDAPI prima che questi messaggi vengano passati ai componenti sopra lo stack (ad esempio Esplora rete o un'applicazione che chiama in WSDAPI).

Il codice XML seguente illustra un elemento AppSequence di esempio. Il prefisso wsd fa riferimento allo spazio dei nomi `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

WSDAPI ignora i messaggi non obsoleti. Per ogni dispositivo (identificato in modo univoco dall'indirizzo dell'endpoint nel corpo SOAP), WSDAPI ignora tutti i messaggi con un valore AppSequence MessageNumber inferiore all'ultimo messaggio visualizzato.

WSDAPI ignora gli annunci XAddr non obsoleti. Se AppSequence InstanceId è inferiore all'ultimo InstanceId visualizzato, WSDAPI ignora gli XAddrs annunciati nel corpo SOAP. Inoltre, se InstanceId è uguale al precedente, ma MetadataVersion è inferiore all'ultimo MetadataVersion, WSDAPI ignora XAddrs.

WSDAPI ignora i messaggi WS-Discovery duplicati. Se vengono inviati WS-Discovery messaggi identici a WSDAPI, verrà elaborato solo il primo messaggio ricevuto. Ciò è in genere rilevante solo per le applicazioni che chiamano direttamente nelle [**interfacce IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) o [**IWSDiscoveryProvider.**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Criteri di individuazione e Exchange dei messaggi](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



