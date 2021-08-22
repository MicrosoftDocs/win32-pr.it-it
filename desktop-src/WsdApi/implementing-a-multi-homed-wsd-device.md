---
description: Questo argomento descrive il supporto di dispositivi multi-homed in WSDAPI e fornisce raccomandazioni di implementazione agli sviluppatori di client e dispositivi.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementazione di un dispositivo WSD multi-homed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ac83b0fe3b951e02e77ef9efc6241ce5a7e1780106b1e85e4f00b987bbbe05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991741"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementazione di un dispositivo WSD multi-homed

[WS-Discovery e](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) il profilo dispositivi per [i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) non descrivono l'implementazione di dispositivi multi-homed. Questo argomento descrive il supporto di dispositivi multi-homed in WSDAPI e fornisce raccomandazioni di implementazione agli sviluppatori di client e dispositivi. In questo argomento si presuppone che i messaggi di individuazione siano inviati tramite IPv4 e IPv6 (se disponibile) con lo stesso ID messaggio e le stesse informazioni di sequenziazione dell'applicazione.

## <a name="discovery-in-a-multi-homed-environment"></a>Individuazione in un ambiente multi-homed

Come accennato [nella sezione Hello](hello-message.md) e [XAddrs](xaddr-validation-rules.md) di [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md), WSDAPI non fornisce mai XAddrs in un messaggio Hello. Ciò significa che lo stesso messaggio Hello può essere inviato su tutte le interfacce di rete con lo stesso ID messaggio e le stesse informazioni di sequenziazione dell'applicazione. In questo modo è più semplice per il rilevamento delle collisioni client rimuovere più messaggi Hello dallo stesso dispositivo quando un client e il dispositivo condividono più subnet.

Poiché gli [XAddrs](xaddr-validation-rules.md) non vengono inviati nel messaggio [Hello,](hello-message.md) le implementazioni client devono inviare un [messaggio Resolve](resolve-message.md) per ottenere l'indirizzo del dispositivo pertinente. La risoluzione deve essere inviata su tutte le interfacce client con lo stesso ID messaggio e il dispositivo deve filtrare i messaggi duplicati in base alle esigenze. L'uso dello stesso ID messaggio per il messaggio Risolvi consente al dispositivo di scegliere un'interfaccia preferita per la comunicazione con i client, se necessario.

Quando si invia [un messaggio ResolveMatch,](resolvematches-message.md) un dispositivo deve fornire [XAddrs](xaddr-validation-rules.md) correlati all'interfaccia di rete su cui è unicasting il messaggio. Questa procedura consente di evitare più tentativi di connessione client e una logica di ripetizione dei tentativi complessa.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Scambio di metadati in un ambiente multi-homed

L'implementazione dello scambio di metadati in un ambiente multi-homed è più difficile rispetto all'implementazione dell'individuazione a causa del controllo delle versioni dei metadati. Se un client richiede metadati su più interfacce, il client può ricevere più [messaggi GetResponse](getresponse--metadata-exchange--message.md) su interfacce diverse. Questi messaggi GetResponse possono contenere sezioni di metadati **relationship** diverse con la stessa versione dei metadati. In questo modo si riduce il valore del numero di versione dei metadati.

Esiste un approccio alternativo, in cui un singolo [messaggio GetResponse](getresponse--metadata-exchange--message.md) viene inviato in risposta con tutti gli indirizzi per il servizio. Lo svantaggio di questo metodo è che le informazioni private, ad esempio la topologia delle reti accessibili indirettamente, possono essere divulgate.

In Windows Vista, i metadati forniti da WSDAPI contengono solo indirizzi validi per l'interfaccia su cui è stata ricevuta la richiesta di metadati.

 

 



