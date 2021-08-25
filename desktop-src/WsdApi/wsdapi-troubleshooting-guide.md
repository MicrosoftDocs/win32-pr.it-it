---
description: Lo scopo di questa guida è aiutare gli utenti a risolvere i problemi riscontrati quando si usano LE API di individuazione WSDAPI, quando si crea un host WSDAPI o un proxy di dispositivo o quando si usano funzioni del sistema operativo (ad esempio Individuazione funzioni o Esplora rete) che si basano su WSDAPI.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: Guida alla risoluzione dei problemi di WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a904b2bf4072721e6c0e9c01191aa1b3d5f55224b096434062b7aa8535fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860033"
---
# <a name="wsdapi-troubleshooting-guide"></a>Guida alla risoluzione dei problemi di WSDAPI

Lo scopo di questa guida è aiutare gli utenti a risolvere gli errori riscontrati quando si usano LE API di individuazione WSDAPI, quando si crea un host WSDAPI o un proxy di dispositivo o quando si usano funzioni del sistema operativo (ad esempio [Individuazione](/previous-versions/windows/desktop/fundisc/fd-portal) funzioni o Esplora rete) che si basano su WSDAPI. L'obiettivo principale è risolvere i problemi quando un client e un host non possono vedersi nella rete.

Per gli utenti WSDAPI, questa guida contiene informazioni che consentono di risolvere correttamente i problemi di un proxy di dispositivo (tramite [**WSDCreateDeviceProxy),**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)un provider di individuazione [**(con WSDCreateDiscoveryProvider)**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)o un editore di individuazione [**(con WSDCreateDiscoveryPublisher).**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)

Questa guida presuppone che sia il client che l'host possano interagire correttamente con WSDAPI in un ambiente controllato. Di conseguenza, questa guida non è destinata a risolvere i problemi degli stack DPWS che potrebbero generare messaggi WS non corretto. Per informazioni sul test dell'interoperabilità con WSDAPI, vedere [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) in Windows Driver Kit (WDK).

Prima di iniziare a risolvere i problemi dell'applicazione, è necessario acquisire familiarità con individuazione e [metadati Exchange modelli di messaggio.](discovery-and-metadata-exchange-message-patterns.md)

Questa guida contiene le sezioni seguenti.

-   [Attività iniziali con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
-   [Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
