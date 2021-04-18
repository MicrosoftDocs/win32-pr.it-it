---
description: Se l'host e il client generici possono vedersi reciprocamente nella rete, ma l'host e il client effettivi non possono, è probabile che il problema si trovi nei messaggi inviati tra gli endpoint sulla rete.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Uso del client di debug WSD per verificare il traffico multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f03e06baefc40bad843a5193b2cec604383251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312671"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>Uso del client di debug WSD per verificare il traffico multicast

Se l'host e il client generici possono vedersi reciprocamente nella rete, ma l'host e il client effettivi non possono, è probabile che il problema si trovi nei messaggi inviati tra gli endpoint sulla rete. Per ulteriori informazioni sull'host e sul client generico, vedere [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md). Poiché le tracce di rete complete possono essere difficili da raccogliere, filtrare e leggere, lo strumento client di debug WSD può essere utilizzato per stampare i lati multicast dei messaggi WS-Discovery.

Il client di debug WSD in modalità multicast può ispezionare solo la metà dei messaggi, poiché il client non è in grado di stampare messaggi unicast. Se il traffico unicast è di interesse, passare direttamente al [controllo delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Questa procedura mostra un metodo che consente di visualizzare tutto il traffico multicast sulla rete. Per visualizzare solo il traffico multicast da e verso il dispositivo, vedere la sezione [Filtering WSD debug client results](#filtering-wsd-debug-client-results) riportata di seguito.

**Per usare il client di debug WSD per verificare il traffico multicast**

1.  Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).
2.  Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe/Mode multicast**
3.  Riprodurre l'errore avviando l'host e il client o premendo F5 in Network Explorer.
4.  Verificare che i messaggi siano multicast.

Se i messaggi richiesti vengono visualizzati nell'output del client di debug WSD, l'errore dell'applicazione potrebbe trovarsi nel contenuto del messaggio multicast o nell'esistenza o nel contenuto dei messaggi di risposta unicast corrispondenti. Continuare la risoluzione dei problemi seguendo le istruzioni riportate in [ispezione delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Se i messaggi richiesti vengono visualizzati nell'output del client di debug WSD, è probabile che l'origine del problema dell'applicazione sia stata identificata. È probabile che il traffico multicast non venga trasmesso sulla rete. Questo errore può verificarsi quando l'applicazione non enumera correttamente gli adapter multicast. Le applicazioni devono inviare in modo esplicito il traffico multicast su tutte le interfacce di rete. in caso contrario, è possibile che i pacchetti non vengano generati per l'interfaccia di loopback o per altre interfacce. Per verificare che i pacchetti non siano visualizzati sulla rete, seguire le istruzioni riportate in [ispezione delle tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) e cercare le evidenze dei messaggi multicast mancanti.

## <a name="verifying-that-messages-are-being-multicast"></a>Verifica del multicast dei messaggi

Verificare sempre che i messaggi [Probe](probe-message.md) siano in multicast. Facoltativamente, verificare che i messaggi [Hello](hello-message.md) e [Resolve](resolve-message.md) siano in multicast. Si noti che non tutte le applicazioni utilizzano i messaggi di risoluzione. Per ulteriori informazioni sui modelli di messaggio utilizzati da client e host, vedere [modelli di messaggio di scambio di metadati e individuazione](discovery-and-metadata-exchange-message-patterns.md) e [Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md).

I messaggi devono essere attivati per poter essere inviati come descritto nel passaggio 3 precedente. Il client di debug WSD Visualizza il messaggio SOAP non elaborato come output. Poiché tutti i messaggi stampati dal client di debug WSD in modalità multicast vengono ricevuti su un socket multicast, l'indirizzo di destinazione del messaggio non viene visualizzato.

L'output del client di debug WSD di esempio seguente mostra un messaggio Probe. L'elemento <wsa: Action> identifica il messaggio come messaggio Probe. Esaminare il campo <wsa: Action> per verificare che il messaggio ricevuto sia un messaggio Probe.

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

L'output del client di debug WSD di esempio seguente mostra un messaggio Hello. L'elemento <wsa: Action> identifica il messaggio come messaggio Hello.

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a>Filtro dei risultati del client di debug WSD

Il filtro dei risultati del client di debug WSD può aiutare a identificare il traffico degli eventi imprevisti che interessa il dispositivo. Il filtro è necessario solo per le reti rumorose.

Esistono due modi per filtrare i risultati. Gli indirizzi IP da filtrare possono essere identificati in modo esplicito all'avvio del client di debug WSD. In alternativa, è possibile specificare gli indirizzi IP dopo l'avvio del client. In questa sezione vengono descritti entrambi i metodi.

**Per specificare gli indirizzi IP da filtrare all'avvio del client di debug WSD**

1.  Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).
2.  Raccogliere gli indirizzi IP del dispositivo. Se il dispositivo dispone di più indirizzi (ad esempio, dispone di indirizzi IPv4 e IPv6) tutti gli indirizzi devono essere raccolti.
3.  Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe/Mode multicast/IP Add***<device IP>*

*<device IP>* è un indirizzo IP. Nell'elenco seguente vengono illustrati alcuni formati di esempio per questo indirizzo IP.

-   192.168.0.1
-   :: 1
-   mydevice.contoso.com

Il client di debug WSD risolve automaticamente i nomi host specificati al prompt dei comandi.

**Per filtrare i risultati dopo l'avvio del client di debug WSD**

1.  Configurare l'host e il client in modo che vengano eseguiti attraverso la rete (ovvero, assicurarsi che l'host e il client operino in computer diversi).
2.  Raccogliere gli indirizzi IP del dispositivo. Se il dispositivo dispone di più indirizzi (ad esempio, dispone di indirizzi IPv4 e IPv6) tutti gli indirizzi devono essere raccolti.
3.  Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe/Mode multicast**
4.  Al prompt dei comandi del client di debug WSD eseguire il comando seguente: **IP Add***<device IP>*
5.  Ripetere il passaggio 4 fino a quando non sono stati aggiunti tutti gli indirizzi IP del dispositivo.

Nella procedura seguente si presuppone che il client di debug WSD sia stato avviato e che il filtro in base all'indirizzo IP sia in corso.

**Per verificare che gli indirizzi IP corretti vengano filtrati**

-   Al prompt dei comandi del client di debug WSD eseguire il comando seguente: **IP Print**

    Viene visualizzato l'elenco degli indirizzi IP da filtrare.

Nella procedura seguente si presuppone che il client di debug WSD sia stato avviato e che il filtro in base all'indirizzo IP sia in corso.

**Per disabilitare il filtro**

-   Al prompt dei comandi del client di debug WSD eseguire il comando seguente: **IP Clear**

    Tutto il traffico multicast verrà ora visualizzato nell'output di debug.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



