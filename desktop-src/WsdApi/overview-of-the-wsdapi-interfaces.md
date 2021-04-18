---
description: Web Services on Devices API (WSDAPI) viene usato per sviluppare applicazioni client che trovano e accedono ai dispositivi e per sviluppare host di dispositivi e servizi associati eseguiti in Windows Vista e Windows Server 2008.
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: Panoramica delle interfacce WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310284"
---
# <a name="overview-of-the-wsdapi-interfaces"></a>Panoramica delle interfacce WSDAPI

Web Services on Devices API (WSDAPI) viene usato per sviluppare applicazioni client che trovano e accedono ai dispositivi e per sviluppare host di dispositivi e servizi associati eseguiti in Windows Vista e Windows Server 2008. L'API di [individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) e lo strumento [WsdCodeGen](web-services-for-devices-code-generator.md) sono strumenti aggiuntivi che possono essere usati per lo sviluppo di client, dispositivi e servizi. Le interfacce WSDAPI possono essere usate direttamente per esporre funzionalità avanzate.

## <a name="major-wsdapi-interfaces"></a>Principali interfacce WSDAPI

Le quattro principali interfacce WSDAPI sono [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider), [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher), [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)e [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost). Per un elenco di tutte le interfacce WSDAPI, vedere [servizi Web sulle interfacce dei dispositivi](web-services-for-devices-interfaces.md).

## <a name="iwsdiscoveryprovider"></a>IWSDiscoveryProvider

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) viene usato per implementare la funzionalità WS-Discovery nei client.

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) emette WS-Discovery [Probe](probe-message.md) e [risolve](resolve-message.md) i messaggi e riceve i messaggi [Hello](hello-message.md), [bye](bye-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) . Usare le informazioni recuperate tramite l'interfaccia **IWSDiscoveryProvider** quando si crea un'interfaccia [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) usata per descrivere e controllare un dispositivo DPWS specifico.

Non è necessaria un'interfaccia [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) quando si risolve semplicemente un particolare indirizzo del dispositivo DPWS prima di creare un proxy di dispositivo. [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) risolverà automaticamente l'indirizzo del dispositivo, se necessario.

L'API di [individuazione della funzione](/previous-versions/windows/desktop/fundisc/fd-portal) può essere usata per l'individuazione di dispositivi e servizi generici, perché l'API può individuare i dispositivi DPWS e anche i dispositivi che usano altri protocolli. Si consiglia di usare l'individuazione della funzione quando si scrive un'applicazione di individuazione generica.

## <a name="iwsdiscoverypublisher"></a>IWSDiscoveryPublisher

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) viene usato per implementare la funzionalità di WS-Discovery nei servizi di destinazione, ad esempio i dispositivi.

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) consente a un'applicazione di pubblicare la propria presenza usando WS-Discovery messaggi Hello e bye. Questa interfaccia consente a un'applicazione di ricevere richieste di probe e di risoluzione e di creare e inviare risposte ProbeMatches e ResolveMatches.

Un'interfaccia [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) non è necessaria quando si pubblica semplicemente l'esistenza di un oggetto [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) . **IWSDDeviceHost** gestisce la propria presenza WS-Discovery.

## <a name="iwsddeviceproxy"></a>IWSDDeviceProxy

[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) viene utilizzato per implementare la funzionalità WS-Discovery, WS-MetadataExchange e Control sul lato client. Questa funzionalità include il canale protetto facoltativo, WS-Eventing e le funzionalità degli allegati.

L'interfaccia [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) dispone dei tre utilizzi seguenti.

-   Risolve gli indirizzi dei dispositivi logici, se necessario.
-   Avvia richieste di metadati ai dispositivi per enumerare i tipi e gli indirizzi dei servizi.
-   Fornisce un'origine per gli oggetti [**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) , che può essere usata per emettere messaggi di controllo per servizi specifici in un dispositivo.

L'oggetto [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) viene in genere creato e utilizzato interamente all'interno del codice generato da [WsdCodeGen](web-services-for-devices-code-generator.md).

## <a name="iwsddevicehost"></a>IWSDDeviceHost

[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) viene utilizzato per implementare la funzionalità WS-Discovery, WS-MetadataExchange e host del servizio sul lato dispositivo. I servizi ospitati possono rispondere ai messaggi di controllo e possono supportare il canale sicuro, WS-Eventing e le funzionalità degli allegati.

L'interfaccia [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) ha gli utilizzi seguenti.

-   Ospita oggetti servizio.
-   Annuncia la presenza di un host dispositivo sulla rete mediante WS-Discovery.
-   Risponde alle richieste di WS-MetadataExchange e descrive i tipi e i percorsi dei servizi ospitati.
-   Invia le richieste di rete in oggetti servizio.

Le funzionalità di gestione delle sottoscrizioni WS-Discovery, WS-MetadataExchange e WS-Eventing vengono gestite interamente nell'oggetto host del dispositivo. Per poter ospitare un servizio all'interno di un host del dispositivo, è necessario soddisfare i requisiti seguenti.

-   L'host deve essere creato chiamando [**WSDCreateDeviceHost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost).
-   I metadati associati al servizio devono essere registrati.
-   Il servizio stesso deve essere registrato.
-   È necessario avviare l'host del dispositivo.

L'oggetto [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) viene in genere creato e utilizzato all'interno del codice generato da [WsdCodeGen](web-services-for-devices-code-generator.md).

 

 
