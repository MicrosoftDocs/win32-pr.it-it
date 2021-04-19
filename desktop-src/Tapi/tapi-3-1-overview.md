---
description: La versione 3,1 di TAPI è un'API basata su COM che unisce la telefonia classica e IP. Le applicazioni possibili variano da chiamate vocali semplici sulla rete PSTN (Public Switched Telephone) a multicast IP multimediale con qualità del servizio (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Panoramica di TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311858"
---
# <a name="tapi-31-overview"></a>Panoramica di TAPI 3,1

La versione 3,1 di TAPI è un'API basata su COM che unisce la telefonia classica e IP. Le applicazioni possibili variano da chiamate vocali semplici sulla rete PSTN (Public Switched Telephone) a multicast IP multimediale con qualità del servizio (QOS).

Per ulteriori informazioni sulle funzionalità di telefonia IP di TAPI 3,1, consultare la pagina relativa alla "telefonia IP con TAPI 3" white paper, disponibile nel sito Web Microsoft.

Sono disponibili quattro componenti principali per TAPI 3,1:

-   API COM
-   Server TAPI
-   Provider di servizi di telefonia (TSPs)
-   Provider di flussi multimediali (MSPs)

Il diagramma seguente illustra l'architettura di TAPI 3,1:

![architettura di TAPI 3](images/callarc-gif-1.png)

L'API viene implementata come un gruppo di oggetti Component Object Model (COM). Lo sviluppo di TAPI nel modello COM orientato a oggetti consente agli sviluppatori di scrivere applicazioni abilitate per TAPI in molti linguaggi, ad esempio Java, Visual Basic o C/C++. L'uso di COM Abilita gli aggiornamenti dei componenti delle funzionalità TAPI.

Il processo del server TAPI (TAPISRV) astrae l'interfaccia del provider di servizi TAPI (TSPI) da TAPI 3. x e TAPI 2. x, consentendo l'uso dei provider di servizi di telefonia TAPI 2. x con TAPI 3. x, mantenendo lo stato interno di TAPI. TAPISRV viene implementato come processo del servizio all'interno di SVCHOST.

[Provider di servizi](./tapi-service-providers.md) meccanismi astratti di trasporto multimediale specifici del provider. Si trovano in genere in coppie, ovvero un provider di servizi di telefonia (TSP) per il controllo delle chiamate e un provider di servizi multimediali (MSP) per il controllo multimediale.

I [provider di servizi di telefonia](./telephony-service-providers-start-page.md) (TSPs) sono responsabili della risoluzione del modello di chiamata indipendente dal protocollo di TAPI in meccanismi di controllo delle chiamate specifici del protocollo. TAPI 3,1 fornisce la compatibilità con le versioni precedenti di TAPI 2,1 TSPs. Per impostazione predefinita, due provider di servizi di telefonia IP (e i MSPs associati) con TAPI 3,1: H. 323 TSP e il TSP per la conferenza multicast IP.

I [provider di servizi multimediali](media-service-providers-start-page.md) (MSPS) forniscono un modo uniforme per accedere ai flussi multimediali in una chiamata, supportando l'API DirectShow<sup>TM</sup> come gestore principale del flusso multimediale. TAPI MSPs implementa le interfacce DirectShow per un determinato TSP e sono necessarie per qualsiasi servizio di telefonia che usa lo streaming DirectShow. I flussi generici vengono gestiti dall'applicazione.

 

 
