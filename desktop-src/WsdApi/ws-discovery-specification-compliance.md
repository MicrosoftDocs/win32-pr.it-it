---
description: 'Altre informazioni su: Conformità WS-Discovery specifica'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: WS-Discovery conformità alle specifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07794140f05a065fb770ae2d5782f24180fb7e7ef66757278d5c5c93a3fd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991411"
---
# <a name="ws-discovery-specification-compliance"></a>WS-Discovery conformità alle specifiche

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) descrive come eseguire le attività seguenti:

-   Annunciare la disponibilità dei servizi nella subnet locale
-   Cercare i servizi nella subnet
-   Individuare un servizio a cui si fa riferimento in precedenza

A tale scopo, WS-Discovery due messaggi unidirezionali, [Hello](hello-message.md) [e Bye,](bye-message.md)e due messaggi di ricerca bidirezionali, [Probe](probe-message.md) e [Resolve.](resolve-message.md)

WS-Discovery fornisce anche indirizzi e una porta riservata per l'individuazione locale dei collegamenti IPv4 e IPv6. La specifica consente anche di definire associazioni alternative altrove, ad esempio l'associazione Probe su HTTP definita nel profilo dispositivi per i servizi [Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).

La WS-Discovery specifica descrive la funzionalità elective usando i termini MAY o SHOULD in una specifica raccomandazione o restrizione di implementazione. La funzionalità omessa può essere una funzionalità descritta come REQUIRED nella specifica WS-Discovery non implementata da WSDAPI oppure può essere una funzionalità implementata da WSDAPI in un metodo diverso da quello specificato nella specifica WS-Discovery.

Questo argomento descrive come WS-Discovery restrizioni, requisiti e funzionalità elective vengono gestite dall'implementazione WSDAPI. Questo argomento è più leggibile in tandem con la WS-Discovery specifica.

## <a name="ws-discovery-and-soap-over-udp-support"></a>WS-Discovery e soap-over-UDP

In SOAP-over-UDP, la sezione 3.2 specifica che il messaggio UDP deve essere contenuto in un datagramma di 64.000. WSDAPI accetterà 64.000 messaggi UDP, ma il vincolo DPWS max \_ ENVELOPE \_ SIZE (32K) vincolerà le dimensioni del messaggio. Come richiesto da [WS-Discovery,](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)WSDAPI supporta i modelli di messaggio descritti nella sezione 4.

È possibile configurare WSDAPI per supportare il modello di sicurezza nelle sezioni 7 e 8. In questo caso, WSDAPI firmerà i messaggi WS-Discovery in uscita e convaliderà le firme nei messaggi in ingresso.

WSDAPI implementa l'algoritmo di ritrasmissione definito nell'appendice I come modificato dall'appendice I di DPWS.

In WS-Discovery WSDAPI usa gli indirizzi specificati nella sezione 2.4. WSDAPI estende APP MAX DELAY dalla sezione 2.4, ma non nella misura definita \_ \_ nell'appendice I di DPWS. Per altre informazioni su APP \_ MAX \_ DELAY, vedere [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md).

WS-Discovery descrive la raccomandazione relativa al formato URI nella sezione `uuid:` 2.6, ma WSDAPI esegue l'override di questa raccomandazione. WSDAPI usa invece il `urn:uuid:` formato URI descritto in DPWS.

La sezione 3 di WS-Discovery descrive come un client interagisce con un proxy di individuazione. WSDAPI non riconosce questa interazione e ignora gli annunci dai proxy di individuazione. In Windows 7, WSDAPI implementa un'estensione privata al protocollo WS-Discovery, WS-Discovery Remote Extensions, per consentire ai client di individuazione di cercare servizi distribuiti in molte reti diverse inviando richieste a proxy centralizzati. Per altre informazioni, vedere [Funzionalità WS-Discovery aggiuntive](additional-ws-discovery-functionality.md).

La sezione 4.1, paragrafo 3 di WS-Discovery richiede che un timer deve trascorrere prima dell'invio di un messaggio [Hello.](hello-message.md) L'API di hosting non attende prima di inviare un messaggio Hello. Se uno scenario richiede un ritardo prima dell'invio di un messaggio Hello, lo sviluppatore dell'applicazione deve implementare un'attesa.

WSDAPI implementa tutti i messaggi descritti in WS-Discovery sezioni 4, 5 e 6. WSDAPI applica anche il TIMEOUT MATCH descritto nella sezione 7 come modificato dall'appendice I. WSDAPI protegge solo da "Replay" dalle considerazioni sulla sicurezza nella sezione \_ 9.

WSDAPI implementa la sequenziazione delle applicazioni come descritto nell'appendice I WS-Discovery.

 

 



