---
description: Lo scopo di questo argomento è descrivere la funzionalità di individuazione implementata da WSDAPI, ma non diversamente descritta nelle specifiche DPWS o WS-Discovery specifiche.
ms.assetid: ae7eff53-c932-4cba-9e71-c60f308f0e2d
title: Funzionalità WS-Discovery aggiuntive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7ee4094950c51ed84724abb9eaea493f7dad7cf7803832fb6e8762fdd99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106779"
---
# <a name="additional-ws-discovery-functionality"></a>Funzionalità WS-Discovery aggiuntive

In alcuni casi, il profilo [dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) e le specifiche correlate non definiscono in modo esplicito la funzionalità di implementazione. Ad esempio, la [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) non definisce il comportamento di client e host in ambienti multi-homed. Al momento dell'implementazione di WSDAPI, alcune funzionalità di individuazione sono state aggiunte oltre a quella definita nella specifica.

WSDAPI implementa anche parti selezionate di WS-Discovery CD1 v1.1 per la comunicazione con un proxy di individuazione su HTTP.

Lo scopo di questo argomento è descrivere la funzionalità di individuazione implementata da WSDAPI, ma non diversamente descritta nelle specifiche DPWS o WS-Discovery specifiche.

## <a name="ipv6-addresses-and-the-soapudp-uri-format"></a>Indirizzi IPv6 e formato URI soap.udp

SOAP-over-UDP e WS-Discovery non descrivono in modo esplicito come viene rappresentato un indirizzo IPv6 letterale nel formato URI soap.udp. [RFC 2396,](https://www.ietf.org/rfc/rfc2396.txt)intitolato "UNIFORM Resource Identifiers (URI): Generic Syntax", indica che gli indirizzi IPv6 letterali non sono supportati dal formato URI soap.udp.

Per semplicità, WSDAPI riconosce gli indirizzi IPv6 racchiusi tra parentesi quadre nello schema soap.udp. Ad esempio, `soap.udp://[2001:abcd:0001:0002:0003:0004:0005:0032]:3702` l'indirizzo viene riconosciuto da WSDAPI. Questo è simile al modo in cui gli indirizzi IPv6 vengono gestiti in HTTP.

## <a name="hello-and-xaddrs"></a>Hello e XAddrs

L'oggetto host DPWS di WSDAPI non invierà mai un messaggio Hello WS-Discovery [con](hello-message.md) [XAddrs](xaddr-validation-rules.md) nel corpo del messaggio. Un client invierà sempre un [messaggio Resolve](resolve-message.md) dopo la ricezione di un messaggio Hello se il client deve ottenere XAddrs.

Questo approccio offre due vantaggi. In primo luogo, un dispositivo basato su WSDAPI non esporrà mai XAddr che divulgano gli indirizzi IP delle reti private. In secondo luogo, un dispositivo basato su WSDAPI espone solo XAddrs accessibili al client, il che significa che gli indirizzi IPv6 non vengono mai inviati a un client IPv4.

Quando viene [ricevuto](probe-message.md) un messaggio probe o resolve, viene inviato un solo XAddr in risposta. L'oggetto XAddr inviato corrisponde all'indirizzo locale in cui è stata ricevuta la richiesta. Se la richiesta è stata ricevuta tra subnet su IPv6, WSDAPI fornirà un indirizzo IPv6 globale nella risposta.

## <a name="preferred-addresses"></a>Indirizzi preferiti

Un dispositivo può fornire più XAddr in un [messaggio Hello,](hello-message.md) [ProbeMatch](probematches-message.md)o [ResolveMatch.](resolvematches-message.md) Un servizio può anche essere disponibile in più endpoint con indirizzi di trasporto diversi. In questi casi, WSDAPI tenterà di comunicare con il dispositivo nel primo indirizzo utilizzabile trovato. Un indirizzo può essere utilizzato se deriva da un protocollo disponibile, ad esempio IPv4 in un computer in cui è installato IPv4 o IPv6 in un computer in cui è installato IPv6. Inoltre, se l'indirizzo proveniva da un dispositivo o un servizio che non si trova nella subnet locale, è utilizzabile solo se è IPv4, sito IPv6 locale o collegamento IPv6 locale.

## <a name="wsdl-in-metadata-exchange"></a>WSDL nello scambio di metadati

I dispositivi e i servizi compilati su WSDAPI non forniscono wsdl nello scambio di metadati a meno che non vengano estesi dall'applicazione per fornire queste informazioni. Per impostazione predefinita, il provisioning WSDL non fa parte del modello di programmazione.

## <a name="app_max_delay"></a>RITARDO \_ MASSIMO \_ APP

DPWS definisce APP MAX DELAY, l'intervallo casuale di ritardo tra la ricezione di un probe e l'invio di \_ \_ [probeMatch,](probematches-message.md)come 5.000 millisecondi. [](probe-message.md) Windows Il firewall richiede che il modello di risposta unicast/richiesta multicast per UDP funzioni solo entro la finestra del firewall di 4 secondi. Di conseguenza, WSDAPI trasmetterà le risposte in un massimo di 2.500 ms anziché nella finestra di 5.000 ms descritta da APP \_ MAX \_ DELAY.

## <a name="iana-port-reservations"></a>Prenotazioni di porte IANA

WSDAPI usa la porta TCP 5357 per il traffico HTTP e la porta TCP 5358 per il traffico HTTPS per impostazione predefinita. Queste porte sono riservate per i processi con privilegi inferiori tramite una prenotazione URL in HTTP.sys e sono riservate anche con IANA.

## <a name="udp-port-sharing"></a>Condivisione delle porte UDP

WSDAPI usa la condivisione delle porte. I messaggi unicast inviati alla porta 3702 potrebbero non essere gestiti correttamente da tutte le applicazioni basate su WSDAPI. Se un'applicazione viene associata esclusivamente alla porta 3702, potrebbe impedire alle applicazioni basate su WSDAPI di usare correttamente tale porta.

## <a name="ws-discovery-v11-cd1-proxy"></a>WS-Discovery proxy CD1 v1.1

WSDAPI cerca e comunica con un proxy di individuazione che implementa WS-Discovery protocollo in modalità gestita CD1 v1.1. WS-Discovery 1.1 CD1 è la prima revisione di WS-Discovery per includere una descrizione esplicita di un protocollo HTTP per la comunicazione tra un proxy e un client o un dispositivo.

Per limitare il numero di versioni simultanee usate nelle richieste multicast, WSDAPI invia una richiesta probe WS-Discovery nello spazio dei nomi 2005/04, ma cerca il tipo DiscoveryProxy CD1 WS-Discovery v1.1. Se un proxy risponde, WSDAPI invierà una richiesta HTTP Probe o Resolve all'endpoint proxy specificato, come definito in WS-Discovery v1.1 CD1.

 

 



