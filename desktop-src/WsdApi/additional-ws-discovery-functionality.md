---
description: Lo scopo di questo argomento è descrivere la funzionalità di individuazione implementata da WSDAPI, ma non diversamente descritta nelle specifiche DPWS o WS-Discovery.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Funzionalità di WS-Discovery aggiuntive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9856605273bec9c757e0b29c389991bf061309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233246"
---
# <a name="additional-ws-discovery-functionality"></a>Funzionalità di WS-Discovery aggiuntive

In alcuni casi, il [profilo dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) e le specifiche correlate non definiscono in modo esplicito le funzionalità di implementazione. Ad esempio, la specifica [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) non definisce il comportamento del client e dell'host negli ambienti multihomed. Quando WSDAPI è stato implementato, alcune funzionalità di individuazione sono state aggiunte oltre la funzionalità definita nella specifica.

WSDAPI implementa anche parti selezionate del CD1 WS-Discovery v 1.1 per la comunicazione con un proxy di individuazione su HTTP.

Lo scopo di questo argomento è descrivere la funzionalità di individuazione implementata da WSDAPI, ma non diversamente descritta nelle specifiche DPWS o WS-Discovery.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>Indirizzi IPv6 e formato URI SOAP. UDP

SOAP-over-UDP e WS-Discovery non descrivono in modo esplicito la modalità di rappresentazione di un indirizzo IPv6 letterale nel formato URI SOAP. UDP. [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), denominato "Uniform Resource Identifier (URI): sintassi generica", indica che gli indirizzi IPv6 letterali non sono supportati dal formato URI SOAP. UDP.

Per semplicità, WSDAPI riconosce gli indirizzi IPv6 racchiusi tra parentesi quadre nello schema SOAP. UDP. Ad esempio, l'indirizzo `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` viene riconosciuto da wsdapi. Questo tipo di gestione è simile a quello degli indirizzi IPv6 gestiti in HTTP.

## <a name="hello-and-xaddrs"></a>Hello e XAddrs

L'oggetto host DPWS di WSDAPI non invierà mai un messaggio WS-Discovery [Hello](hello-message.md) con [XAddrs](xaddr-validation-rules.md) nel corpo del messaggio. Un client invierà sempre un messaggio di [risoluzione](resolve-message.md) dopo la ricezione di un messaggio Hello se il client deve ottenere il XAddrs.

Questo approccio presenta due vantaggi. In primo luogo, un dispositivo basato su WSDAPI non esporrà mai XAddrs che divulgano gli indirizzi IP delle reti private. In secondo luogo, un dispositivo basato su WSDAPI espone solo XAddrs accessibili al client, il che significa che gli indirizzi IPv6 non vengono mai inviati a un client IPv4.

Quando viene ricevuto un [Probe](probe-message.md) o un messaggio di risoluzione, viene inviato solo un singolo XAddr in risposta. Il XAddr inviato corrisponde all'indirizzo locale su cui è stata ricevuta la richiesta. Se la richiesta è stata ricevuta tra subnet su IPv6, WSDAPI fornirà un indirizzo IPv6 globale nella risposta.

## <a name="preferred-addresses"></a>Indirizzi preferiti

Un dispositivo può fornire più XAddrs in un messaggio [Hello](hello-message.md), [ProbeMatch](probematches-message.md)o [ResolveMatch](resolvematches-message.md) . Un servizio può essere disponibile anche in più endpoint con indirizzi di trasporto diversi. In questi casi, WSDAPI proverà a comunicare con il dispositivo sul primo indirizzo utilizzabile che trova. Un indirizzo può essere utilizzato se è un protocollo disponibile, ad esempio IPv4 in un computer in cui è installato IPv4 o IPv6 in un computer in cui è installato IPv6. Inoltre, se l'indirizzo proviene da un dispositivo o un servizio che non si trova nella subnet locale, può essere utilizzato solo se è IPv4, sito IPv6 locale o collegamento IPv6 locale.

## <a name="wsdl-in-metadata-exchange"></a>WSDL nello scambio di metadati

I dispositivi e i servizi basati su WSDAPI non forniscono il proprio WSDL nello scambio di metadati, a meno che l'applicazione non fornisca queste informazioni. Per impostazione predefinita, il provisioning WSDL non fa parte del modello di programmazione.

## <a name="app_max_delay"></a>\_ritardo massimo \_ app

DPWS definisce \_ \_ il ritardo massimo dell'app, l'intervallo casuale per ritardare la ricezione di un [Probe](probe-message.md) e l'invio di un [ProbeMatch](probematches-message.md), come 5.000 millisecondi. Windows Firewall richiede che il modello di risposta multicast request/unicast per UDP funzioni solo all'interno della finestra del firewall di 4 secondi. Di conseguenza, WSDAPI trasmetterà le risposte in 2.500 ms o meno, invece della finestra 5.000 ms descritta dal \_ ritardo massimo dell'app \_ .

## <a name="iana-port-reservations"></a>Prenotazioni di porte IANA

WSDAPI usa la porta TCP 5357 per il traffico HTTP e la porta TCP 5358 per il traffico HTTPS per impostazione predefinita. Queste porte sono riservate per i processi con privilegi più bassi tramite una prenotazione URL in HTTP.sys e sono riservate anche con IANA.

## <a name="udp-port-sharing"></a>Condivisione porte UDP

WSDAPI usa la condivisione delle porte. I messaggi unicast inviati alla porta 3702 potrebbero non essere gestiti correttamente da tutte le applicazioni basate su WSDAPI. Se un'applicazione viene associata esclusivamente alla porta 3702, può impedire che le applicazioni basate su WSDAPI utilizzino correttamente tale porta.

## <a name="ws-discovery-v11-cd1-proxy"></a>Proxy CD1 WS-Discovery v 1.1

WSDAPI cercherà e comunicherà con un proxy di individuazione che implementi il protocollo della modalità gestita di WS-Discovery v 1.1 CD1. WS-Discovery v 1.1 CD1 è la prima revisione di WS-Discovery includere una descrizione esplicita di un protocollo HTTP per la comunicazione tra un proxy e un client o un dispositivo.

Per limitare il numero di versioni simultanee usate nelle richieste multicast, WSDAPI invia una richiesta di probe di WS-Discovery nello spazio dei nomi 2005/04, ma cerca il tipo di DiscoveryProxy CD1 WS-Discovery v 1.1. Se un proxy risponde, WSDAPI invierà un probe HTTP o risolvono la richiesta all'endpoint proxy specificato come definito in WS-Discovery v 1.1 CD1.

 

 



