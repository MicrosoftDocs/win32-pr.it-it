---
description: Se l'host generico e il client possono vedere l'un l'altro nella rete, ma l'host e il client effettivi non possono, è probabile che il problema si trova nei messaggi inviati tra gli endpoint in rete.
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: Uso del client di debug WSD per verificare il traffico multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a814ac97512ef4b0691c22d3238d151372023a7
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380665"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a>Uso del client di debug WSD per verificare il traffico multicast

Se l'host generico e il client possono vedersi in rete, ma l'host e il client effettivi non possono, è probabile che il problema si trova nei messaggi inviati tra gli endpoint in rete. Per altre informazioni sull'host e sul client generici, vedere Uso di un [host generico e di un client per UDP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md) Poiché le tracce di rete complete possono essere difficili da raccogliere, filtrare e leggere, lo strumento client di debug WSD può essere usato per stampare i lati multicast dei WS-Discovery messaggi.

Il client di debug WSD in modalità multicast può controllare solo metà dei messaggi, poiché il client non può stampare messaggi unicast. Se il traffico unicast è di interesse, passare direttamente a [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Questa procedura illustra un metodo che visualizza tutto il traffico multicast sulla rete. Per visualizzare solo il traffico multicast da e verso il dispositivo, vedere la sezione Filtro dei risultati del client di [debug WSD](#filtering-wsd-debug-client-results) riportata di seguito.

**Per usare il client di debug WSD per verificare il traffico multicast**

1.  Configurare l'host e il client per l'esecuzione in rete, ovvero assicurarsi che l'host e il client funzionino in computer diversi.
2.  Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe multicast /mode**
3.  Riprodurre l'errore avviando l'host e il client o premendo F5 nel Esplora rete.
4.  Verificare che i messaggi siano multicast.

Se i messaggi necessari vengono visualizzati nell'output del client di debug WSD, l'errore dell'applicazione potrebbe essere nel contenuto del messaggio multicast o nell'esistenza o nel contenuto dei messaggi di risposta unicast corrispondenti. Continuare la risoluzione dei problemi seguendo le istruzioni in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Se i messaggi necessari vengono visualizzati nell'output del client di debug WSD, è probabile che sia stata identificata l'origine del problema dell'applicazione. È probabile che il traffico multicast non venga trasmesso in rete. Questo errore può verificarsi quando l'applicazione non enumera correttamente gli adattatori multicast. Le applicazioni devono inviare in modo esplicito il traffico multicast su tutte le interfacce di rete. In caso contrario, i pacchetti potrebbero non essere generati per l'interfaccia di loopback o per altre interfacce. Per verificare che i pacchetti non siano visualizzati nella rete, seguire le istruzioni in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) (Ispezione delle tracce di rete per UDP WS-Discovery) e cercare le prove di messaggi multicast mancanti.

## <a name="verifying-that-messages-are-being-multicast"></a>Verifica del multicast dei messaggi

Verificare sempre che [i messaggi probe](probe-message.md) siano multicast. Facoltativamente, verificare che [i messaggi Hello](hello-message.md) e [Resolve](resolve-message.md) siano multicast. Si noti che non tutte le applicazioni usano Risolvi messaggi. Per altre informazioni sui modelli di messaggio [](discovery-and-metadata-exchange-message-patterns.md) usati da client e host, vedere Modelli di messaggi di individuazione e scambio di metadati e Attività iniziali risoluzione dei problemi [WSDAPI.](getting-started-with-wsdapi-troubleshooting.md)

I messaggi devono essere attivati per poter essere inviati come descritto nel passaggio 3 precedente. WSD Debug Client visualizza il messaggio SOAP non elaborato come output. Poiché tutti i messaggi stampati da WSD Debug Client in modalità multicast vengono ricevuti tramite un socket multicast, l'indirizzo di destinazione del messaggio non viene visualizzato.

L'output del client di debug WSD di esempio seguente mostra un messaggio probe. \<wsa:Action>L'elemento identifica il messaggio come messaggio probe. Esaminare il \<wsa:Action> campo per verificare che il messaggio ricevuto sia un messaggio probe.

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

L'output del client di debug WSD di esempio seguente mostra un messaggio Hello. \<wsa:Action>L'elemento identifica il messaggio come messaggio Hello.

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

L'applicazione di filtri ai risultati del client di debug di WSD consente di identificare il traffico degli eventi imprevisti che interessa il dispositivo. Il filtro è necessario solo nelle reti rumorose.

Esistono due modi per filtrare i risultati. Gli indirizzi IP da filtrare possono essere identificati in modo esplicito all'avvio del client di debug WSD. In alternativa, gli indirizzi IP possono essere specificati dopo l'avvio del client. In questa sezione vengono descritti entrambi i metodi.

**Per specificare gli indirizzi IP da filtrare all'avvio del client di debug WSD**

1.  Configurare l'host e il client per l'esecuzione in rete, ovvero assicurarsi che l'host e il client funzionino in computer diversi.
2.  Raccogliere gli indirizzi IP del dispositivo. Se il dispositivo ha più indirizzi (ad esempio, ha indirizzi IPv4 e IPv6), tutti gli indirizzi devono essere raccolti.
3.  Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe /mode multicast /ip add***<device IP>*

*<device IP>* è un indirizzo IP. L'elenco seguente mostra alcuni formati di esempio per questo indirizzo IP.

-   192.168.0.1
-   ::1
-   mydevice.contoso.com

Il client di debug WSD risolve automaticamente i nomi host specificati al prompt dei comandi.

**Per filtrare i risultati dopo l'avvio del client di debug WSD**

1.  Configurare l'host e il client per l'esecuzione in rete, ovvero assicurarsi che l'host e il client funzionino in computer diversi.
2.  Raccogliere gli indirizzi IP del dispositivo. Se il dispositivo ha più indirizzi (ad esempio, ha indirizzi IPv4 e IPv6), tutti gli indirizzi devono essere raccolti.
3.  Aprire un prompt dei comandi ed eseguire il comando seguente: **WSDDebug \_client.exe multicast /mode**
4.  Al prompt dei comandi WSD Debug Client eseguire il comando seguente: **ip add***<device IP>*
5.  Ripetere il passaggio 4 fino a quando non sono stati aggiunti tutti gli indirizzi IP del dispositivo.

Nella procedura seguente si presuppone che il client di debug WSD sia stato avviato e che il filtro in base all'indirizzo IP sia in corso.

**Per verificare che vengano filtrati gli indirizzi IP corretti**

-   Al prompt dei comandi del client di debug WSD eseguire il comando seguente: **ip print**

    Viene visualizzato l'elenco degli indirizzi IP filtrati.

Nella procedura seguente si presuppone che il client di debug WSD sia stato avviato e che il filtro in base all'indirizzo IP sia in corso.

**Per disabilitare il filtro**

-   Al prompt dei comandi WSD Debug Client eseguire il comando seguente: **ip clear**

    Tutto il traffico multicast verrà ora visualizzato nell'output di debug.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali risoluzione dei problemi relativi a WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



