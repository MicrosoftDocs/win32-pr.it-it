---
description: Lo scopo di questa guida è aiutare gli utenti a risolvere gli errori riscontrati quando si usano le API di individuazione WSDAPI, durante la creazione di un host WSDAPI o di un proxy di dispositivo o quando si usano funzioni del sistema operativo, ad esempio l'individuazione di funzioni o Network Explorer, che si basano su WSDAPI.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: Guida alla risoluzione dei problemi di WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c28e9a1fe4cc5b24b386cfb88e39276edc14cb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309738"
---
# <a name="wsdapi-troubleshooting-guide"></a>Guida alla risoluzione dei problemi di WSDAPI

Lo scopo di questa guida è aiutare gli utenti a risolvere gli errori riscontrati quando si usano le API di individuazione WSDAPI, durante la creazione di un host WSDAPI o di un proxy di dispositivo o quando si usano funzioni del sistema operativo, ad esempio l' [individuazione di funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) o Network Explorer, che si basano su wsdapi. L'obiettivo principale è consentire la risoluzione dei problemi quando un client e un host non possono vedersi reciprocamente sulla rete.

Per gli utenti di WSDAPI, questa guida contiene informazioni che consentono di risolvere i problemi relativi a un proxy di dispositivo (mediante [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)), a un provider di individuazione (mediante [**WSDCreateDiscoveryProvider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)) o a un server di pubblicazione di individuazione (tramite [**WSDCreateDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)).

In questa guida si presuppone che il client e l'host possano interagire correttamente con WSDAPI in un ambiente controllato. Di conseguenza, questa guida non è destinata a risolvere i problemi relativi agli stack DPWS che potrebbero generare messaggi WS non appropriati. Per informazioni sull'interoperabilità dei test con WSDAPI, vedere lo [strumento WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) in Windows Driver Kit (WDK).

Prima di iniziare la risoluzione dei problemi dell'applicazione, è necessario acquisire familiarità con i [modelli di messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md).

Questa guida contiene le sezioni seguenti.

-   [Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
-   [Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
