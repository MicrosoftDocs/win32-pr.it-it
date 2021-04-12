---
description: In questo argomento viene descritto il supporto dei dispositivi multihomed in WSDAPI e vengono fornite indicazioni sull'implementazione per gli sviluppatori di client e dispositivi.
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: Implementazione di un dispositivo WSD multihomed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3537b96a577db47419d55cb5c6f732f8f7906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233664"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>Implementazione di un dispositivo WSD multihomed

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) e [Device Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) non descrivono l'implementazione di dispositivi multihomed. In questo argomento viene descritto il supporto dei dispositivi multihomed in WSDAPI e vengono fornite indicazioni sull'implementazione per gli sviluppatori di client e dispositivi. In questo argomento si presuppone che i messaggi di individuazione vengano inviati su IPv4 e IPv6 (se disponibili) con lo stesso ID messaggio e le informazioni di sequenziazione dell'applicazione.

## <a name="discovery-in-a-multi-homed-environment"></a>Individuazione in un ambiente multihomed

Come indicato nella sezione [Hello](hello-message.md) e [XAddrs](xaddr-validation-rules.md) della [funzionalità WS-Discovery aggiuntive](additional-ws-discovery-functionality.md), WSDAPI non fornisce mai XAddrs in un messaggio Hello. Ciò significa che è possibile inviare lo stesso messaggio Hello su tutte le interfacce di rete con lo stesso ID messaggio e le informazioni di sequenziazione dell'applicazione. Questo rende più semplice per il rilevamento di conflitti client eliminare più messaggi Hello dallo stesso dispositivo quando un client e il dispositivo condividono più subnet.

Poiché [XAddrs](xaddr-validation-rules.md) non vengono inviati nel messaggio [Hello](hello-message.md) , le implementazioni client devono inviare un messaggio di [risoluzione](resolve-message.md) per ottenere l'indirizzo del dispositivo pertinente. La risoluzione deve essere inviata su tutte le interfacce client con lo stesso ID messaggio e il dispositivo deve filtrare i messaggi duplicati in base alle esigenze. L'utilizzo dello stesso ID messaggio per il messaggio di risoluzione consente al dispositivo di scegliere un'interfaccia preferita per la comunicazione con i client, se necessario.

Quando si invia un messaggio [ResolveMatch](resolvematches-message.md) , un dispositivo deve fornire [XAddrs](xaddr-validation-rules.md) correlate all'interfaccia di rete su cui è in corso l'unicasting del messaggio. Questa procedura consente di evitare più tentativi di connessione client e la logica di ripetizione dei tentativi complessa.

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>Scambio di metadati in un ambiente multihomed

L'implementazione dello scambio di metadati in un ambiente multihomed è più difficile rispetto all'implementazione dell'individuazione a causa del controllo delle versioni dei metadati. Se un client richiede metadati su più interfacce, il client può ricevere più messaggi [GetResponse](getresponse--metadata-exchange--message.md) su interfacce differenti. Questi messaggi GetResponse possono contenere sezioni di metadati di **relazione** diverse con la stessa versione dei metadati. In questo modo si riduce il valore del numero di versione dei metadati.

Esiste un approccio alternativo, in cui un singolo messaggio [GetResponse](getresponse--metadata-exchange--message.md) viene inviato in risposta con tutti gli indirizzi del servizio. Lo svantaggio di questo metodo è che le informazioni private, ad esempio la topologia di reti indirettamente accessibili, possono essere divulgate.

In Windows Vista, i metadati forniti da WSDAPI contengono solo indirizzi validi per l'interfaccia su cui è stata ricevuta la richiesta di metadati.

 

 



