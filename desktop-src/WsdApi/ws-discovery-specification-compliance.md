---
description: 'Altre informazioni su: conformità della specifica WS-Discovery'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: Conformità della specifica WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcae062448b1913f0cc62dff3b6c86b98280a902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401561"
---
# <a name="ws-discovery-specification-compliance"></a>Conformità della specifica WS-Discovery

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) descrive come eseguire le attività seguenti:

-   Annunciare la disponibilità dei servizi nella subnet locale
-   Cercare i servizi nella subnet
-   Individuare un servizio a cui si fa riferimento in precedenza

A tale scopo, WS-Discovery definisce messaggi di tipo 2 1, [Hello](hello-message.md) e [bye](bye-message.md)e due messaggi di ricerca bidirezionali, [Probe](probe-message.md) e [Risolvi](resolve-message.md).

WS-Discovery fornisce anche indirizzi e una porta riservata per l'individuazione locale dei collegamenti IPv4 e IPv6. La specifica consente inoltre di definire altre associazioni alternative, ad esempio il probe sul binding HTTP definito nel [profilo dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).

La specifica WS-Discovery descrive la funzionalità elettiva usando i termini che possono o devono essere inclusi in una specifica raccomandazione o restrizione di implementazione. La funzionalità omessa può essere una funzionalità descritta come obbligatoria nella specifica WS-Discovery che non è stata implementata da WSDAPI o può essere una funzionalità implementata da WSDAPI in un metodo diverso da quello specificato nella specifica WS-Discovery.

In questo argomento viene descritto come WS-Discovery restrizioni, i requisiti e le funzionalità elettive vengono gestiti dall'implementazione di WSDAPI. Questo argomento viene letto meglio in tandem con la specifica WS-Discovery.

## <a name="ws-discovery-and-soap-over-udp-support"></a>Supporto di WS-Discovery e SOAP-over-UDP

In SOAP-over-UDP la sezione 3,2 specifica che il messaggio UDP deve rientrare in un datagramma 64K. WSDAPI accetterà i messaggi UDP 64K, ma il vincolo DPWS della \_ dimensione massima della busta \_ (32K) vincola le dimensioni del messaggio. Come richiesto da [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), WSDAPI supporta i modelli di messaggio descritti nella sezione 4.

WSDAPI può essere configurato per supportare il modello di sicurezza nelle sezioni 7 e 8. Quando tale configurazione è configurata, WSDAPI firmerà i messaggi in uscita WS-Discovery e convaliderà le firme per i messaggi in ingresso.

WSDAPI implementa l'algoritmo di ritrasmissione definito nell'appendice I come modificato dall'appendice I di DPWS.

In WS-Discovery WSDAPI usa gli indirizzi specificati nella sezione 2,4. WSDAPI estende \_ \_ il ritardo massimo dell'app dalla sezione 2,4, ma non nell'extent come definito nell'appendice i di DPWS. Per altre informazioni sul \_ ritardo massimo delle app \_ , vedere [funzionalità WS-Discovery aggiuntive](additional-ws-discovery-functionality.md).

WS-Discovery descrive la `uuid:` raccomandazione del formato URI nella sezione 2,6, ma WSDAPI esegue l'override di questa raccomandazione. WSDAPI usa invece il `urn:uuid:` formato URI descritto in DPWS.

Nella sezione 3 di WS-Discovery viene descritto il modo in cui un client interagisce con un proxy di individuazione. WSDAPI non riconosce questa interazione e ignora gli annunci da proxy di individuazione. In Windows 7, WSDAPI implementa un'estensione privata per il protocollo WS-Discovery, WS-Discovery estensioni remote, per consentire ai client di individuazione di cercare i servizi distribuiti in molte reti diverse inviando richieste ai proxy centralizzati. Per ulteriori informazioni, vedere [funzionalità WS-Discovery aggiuntive](additional-ws-discovery-functionality.md).

La sezione 4,1, paragrafo 3 di WS-Discovery richiede che un timer debba trascorrere prima che venga inviato un messaggio [Hello](hello-message.md) . L'API di hosting non attende prima di inviare un messaggio Hello. Se uno scenario richiede un ritardo prima che venga inviato un messaggio Hello, lo sviluppatore dell'applicazione deve implementare un'attesa.

WSDAPI implementa tutti i messaggi descritti in WS-Discovery sezioni 4, 5 e 6. WSDAPI applica anche il timeout delle CORRISPONDEnze \_ descritto nella sezione 7, come modificato da DPWS appendice i. WSDAPI protegge solo dalla "riproduzione" dalle considerazioni sicure riportate nella sezione 9.

WSDAPI implementa la sequenziazione dell'applicazione come descritto in WS-Discovery appendice I.

 

 



