---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi delle applicazioni WSDAPI.
ms.assetid: befe4234-8d3a-4fc5-9a7d-faca94964af6
title: Risoluzione dei problemi relativi ad altre applicazioni WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a421f26237cc14d07a43e00faeb6d8bf49aa02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308834"
---
# <a name="troubleshooting-other-wsdapi-applications"></a>Risoluzione dei problemi relativi ad altre applicazioni WSDAPI

Le applicazioni possono chiamare direttamente le interfacce e le funzioni WSDAPI per eseguire l'individuazione dei dispositivi e lo scambio di metadati. I modelli di messaggio utilizzati da queste applicazioni variano.

L'obiettivo di questa guida alla risoluzione dei problemi è aiutare gli sviluppatori di applicazioni WSDAPI a implementare correttamente un proxy di dispositivo. Questa guida non è destinata a risolvere tutti gli aspetti di WSDAPI. Se il proxy del dispositivo è stato creato correttamente e il client e l'host possono vedersi reciprocamente sulla rete, questa guida non può risolvere i problemi dell'applicazione. Per risolvere i problemi relativi all'applicazione, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft per ulteriore assistenza.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxy"></a>Risoluzione dei problemi dei client che chiamano WSDCreateDeviceProxy

Le applicazioni chiamano [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) per creare e inizializzare un'istanza dell'interfaccia [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . Questo oggetto proxy del dispositivo può essere usato per annunciare i servizi in un dispositivo e anche per scambiare i metadati.

Un'applicazione che chiama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) usa sempre i messaggi seguenti.

-   [Recupero](get--metadata-exchange--http-request-and-message.md)
-   [GetResponse](getresponse--metadata-exchange--message.md)

Un'applicazione che chiama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) a volte usa i messaggi seguenti.

-   [Risolvi](resolve-message.md)
-   [ResolveMatches](resolvematches-message.md)

I messaggi [Resolve](resolve-message.md) e [ResolveMatches](resolvematches-message.md) vengono generati quando un indirizzo di dispositivo logico, ovvero un indirizzo del dispositivo con formato urn: UUID: {Guid}, viene passato a *pszDeviceId*. Questi messaggi non vengono generati quando un indirizzo di dispositivo fisico viene passato a *pszDeviceId*. Quando si usano i messaggi Resolve e ResolveMatches, vengono inviati prima dei messaggi [Get](get--metadata-exchange--http-request-and-message.md) e [GetResponse](getresponse--metadata-exchange--message.md) .

È consigliabile usare le procedure di diagnostica seguenti (in ordine) per identificare i problemi di un'applicazione che chiama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) con un indirizzo di dispositivo fisico.

1.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
2.  [Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).

È consigliabile usare le procedure di diagnostica seguenti (in ordine) per identificare i problemi di un'applicazione che chiama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) con un indirizzo di dispositivo logico.

1.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
2.  [Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).

Verificare che i messaggi [Resolve](resolve-message.md) e [ResolveMatches](resolvematches-message.md) vengano generati e soddisfino i requisiti di traffico. Non è necessario cercare i messaggi [Probe](probe-message.md) o [ProbeMatches](probematches-message.md) nell'output del client di debug WSD o nelle tracce di rete.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxyadvanced"></a>Risoluzione dei problemi dei client che chiamano WSDCreateDeviceProxyAdvanced

Le applicazioni chiamano [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) per creare e inizializzare un'istanza dell'interfaccia [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . A differenza di [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy), **WSDCreateDeviceProxyAdvanced** dispone di un parametro *pDeviceAddress* usato per definire l'indirizzo di trasporto del dispositivo. Se viene specificato questo indirizzo di trasporto, la risoluzione degli indirizzi logici non è obbligatoria e i messaggi [Risolvi](resolve-message.md) e [ResolveMatches](resolvematches-message.md) non vengono generati.

Se *pDeviceAddress* è impostato su **null** e *pszDeviceId* è un indirizzo logico, viene richiesta la risoluzione dell'indirizzo e vengono generati i [messaggi di risoluzione e di](resolve-message.md) [ResolveMatches](resolvematches-message.md) .

È consigliabile usare le procedure di diagnostica seguenti (in ordine) per identificare i problemi di un'applicazione che chiama [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) con un parametro _pDeviceAddress_ non **null**. Queste procedure possono essere usate anche quando *pDeviceAddress* è **null** e *pszDeviceId* è un indirizzo fisico.

1.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
2.  [Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).

È consigliabile usare le procedure di diagnostica seguenti (in ordine) per identificare i problemi di un'applicazione che chiama [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) con *PDeviceAddress* impostato su **null** e con *pszDeviceId* impostato su un indirizzo logico.

1.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
2.  [Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).

Verificare che i messaggi [Resolve](resolve-message.md) e [ResolveMatches](resolvematches-message.md) vengano generati e soddisfino i requisiti di traffico. Non è necessario cercare i messaggi [Probe](probe-message.md) o [ProbeMatches](probematches-message.md) nell'output del client di debug WSD o nelle tracce di rete.

## <a name="troubleshooting-clients-using-the-iwsdiscoveryprovider-interface"></a>Risoluzione dei problemi relativi ai client tramite l'interfaccia IWSDiscoveryProvider

Le applicazioni che chiamano l'interfaccia [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) non eseguono lo scambio di metadati. Questa interfaccia viene utilizzata solo per l'individuazione. I modelli di messaggio e le procedure di risoluzione dei problemi sono diversi per ogni metodo chiamato sull'interfaccia **IWSDiscoveryProvider** .

Quando un'applicazione chiama [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype), viene generato un messaggio [Probe](probe-message.md) . Il messaggio Probe viene inviato dal multicast UDP alla porta 3702. Viene generato un messaggio [ProbeMatches](probematches-message.md) in risposta. Il messaggio ProbeMatches viene inviato dall'unicast UDP e ha origine dalla porta 3702.

Quando un'applicazione chiama [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid), viene generato un messaggio di [risoluzione](resolve-message.md) . Un messaggio di risoluzione viene inviato dal multicast UDP alla porta 3702. Viene generato un messaggio [ResolveMatches](resolvematches-message.md) in risposta. ResolveMatches viene inviato da unicast UDP e ha origine dalla porta 3702.

Per identificare i problemi di un'applicazione che chiama [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) o [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid), è necessario usare le procedure di diagnostica seguenti (in ordine). Verificare che i messaggi generati dall'API chiamata soddisfino i requisiti di traffico.

1.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
2.  [Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).

Se un'applicazione chiama [**IWSDiscoveryProvider:: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress), si tratta di un'applicazione di individuazione diretta. Per ulteriori informazioni sulla risoluzione dei problemi, vedere [risoluzione dei problemi relativi alle applicazioni mediante l'individuazione diretta](troubleshooting-applications-using-directed-discovery.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



