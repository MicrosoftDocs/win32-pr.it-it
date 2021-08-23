---
description: TAPI versione 3.1 è un'API basata su COM che unisce la telefonia CLASSICA e IP. Le possibili applicazioni variano da semplici chiamate vocali tramite rete PSTN (Public Switched Telephone Network) a conferenze IP multimediali multicast con qualità del servizio (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Panoramica di TAPI 3.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55aff75690894cc8c8a0d5e692b0c9b019a39116a617dbf2a4ae050200f6892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139899"
---
# <a name="tapi-31-overview"></a>Panoramica di TAPI 3.1

TAPI versione 3.1 è un'API basata su COM che unisce la telefonia CLASSICA e IP. Le possibili applicazioni variano da semplici chiamate vocali tramite rete PSTN (Public Switched Telephone Network) a conferenze IP multimediali multicast con qualità del servizio (QOS).

Per altre informazioni sulle funzionalità di telefonia IP TAPI 3.1, vedere il white paper "Telefonia IP con TAPI 3", disponibile nel sito Web Microsoft.

Per TAPI 3.1 sono disponibili quattro componenti principali:

-   COM API
-   TAPI Server
-   Provider di servizi di telefonia (TSP)
-   Provider di flussi multimediali (MSP)

Il diagramma seguente illustra l'architettura TAPI 3.1:

![Architettura tapi 3](images/callarc-gif-1.png)

L'API viene implementata come una suite di Component Object Model (COM). Lo spostamento di TAPI nel modello COM orientato a oggetti consente agli sviluppatori di scrivere applicazioni abilitate per TAPI in molti linguaggi, ad esempio Java, Visual Basic o C/C++. L'uso di COM abilita gli aggiornamenti dei componenti delle funzionalità TAPI.

Il processo TAPI Server (TAPISRV) astrae TAPI Service Provider Interface (TSPI) da TAPI 3.x e TAPI 2.x, consentendo l'uso dei provider di servizi di telefonia TAPI 2.x con TAPI 3.x, mantenendo lo stato interno di TAPI. TAPISRV viene implementato come processo di servizio all'interno di SVCHOST.

[I provider di servizi](./tapi-service-providers.md) astrattano i meccanismi di trasporto multimediale specifici del provider. In genere sono presenti in coppie: un provider di servizi di telefonia (TSP) per il controllo delle chiamate e un provider di servizi multimediali (MSP) per il controllo multimediale.

[I provider di servizi](./telephony-service-providers-start-page.md) di telefonia (TSP) sono responsabili della risoluzione del modello di chiamata indipendente dal protocollo di TAPI in meccanismi di controllo delle chiamate specifici del protocollo. TAPI 3.1 offre la compatibilità con le versioni precedenti con i TSP TAPI 2.1. Due provider di servizi di telefonia IP (e i relativi PROVIDER di servizi di telefonia IP associati) vengono forniti per impostazione predefinita con TAPI 3.1: il provider di servizi di conferenza H.323 e il provider di servizi di conferenza multicast IP.

[I](media-service-providers-start-page.md) provider di servizi multimediali (MSP) forniscono un modo uniforme per accedere ai flussi multimediali in una chiamata, supportando l'API<sup>TM</sup> DirectShow come gestore del flusso multimediale primario. Gli MSP TAPI implementano DirectShow per un TSP specifico e sono necessari per qualsiasi servizio di telefonia che usa DirectShow streaming. I flussi generici vengono gestiti dall'applicazione.

 

 
