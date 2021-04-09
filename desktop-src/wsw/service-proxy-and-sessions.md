---
title: Proxy e sessioni del servizio
description: Il proxy del servizio ha comportamenti speciali per i binding di canale di sessione e non basati sulla sessione.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Servizi Web per proxy e sessioni del servizio per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047615"
---
# <a name="service-proxy-and-sessions"></a>Proxy e sessioni del servizio

Il [proxy del servizio](service-proxy.md) ha comportamenti speciali per i binding di canale di sessione e non basati sulla sessione. Il proxy del servizio fornisce la semantica basata sulla sessione se l'associazione di canale sottostante è basata sulla sessione. In questo caso viene usato un solo canale per le chiamate di servizio. Tuttavia, se l'associazione di canale non è basata sulla sessione, il proxy del servizio crea un canale separato per ogni chiamata. Si noti, tuttavia, che i canali non basati sulla sessione sono in pool e potrebbero essere riutilizzati. Quando si riutilizza un canale, il proxy del servizio mantiene il canale aperto se il canale sottostante non ha avuto errori o la chiamata su un canale ha causato l'errore del proxy del servizio nel canale. Si noti che. tranne che in caso di errore, dopo l'apertura di un canale viene mantenuto aperto finché il proxy del servizio è aperto e chiuso solo quando il proxy del servizio viene chiuso.


Se l'associazione di canale è basata sulla sessione e in caso di errori del canale sottostante, la macchina a Stati del proxy del servizio passerà allo stato di [**\_ \_ \_ \_ errore del proxy del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) . Nel caso di un'associazione di canale non basata sulla sessione, un errore nel canale sottostante non determina la transizione del proxy allo stato **di \_ \_ \_ \_ errore del proxy del servizio WS** .

Per ulteriori informazioni sul proxy del servizio e sulla relativa relazione con lo stato, vedere l'argomento relativo al [proxy del servizio](service-proxy.md) . Per esempi di diverse associazioni di canale, vedere gli esempi seguenti:

-   binding di canale non di sessione, [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   associazione di canale basata sulla sessione, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




