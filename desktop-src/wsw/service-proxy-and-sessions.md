---
title: Proxy del servizio e sessioni
description: Il proxy del servizio ha comportamenti speciali per le associazioni di canale non basate su sessione e sessione.
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- Proxy di servizio e servizi Web sessioni per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d845bd341f1343338031619a72fd5dbd307fe1a92175b3753d83b373d73c812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962890"
---
# <a name="service-proxy-and-sessions"></a>Proxy del servizio e sessioni

Il [proxy del](service-proxy.md) servizio ha comportamenti speciali per le associazioni di canale non basate su sessione e sessione. Il proxy del servizio fornisce la semantica basata su sessione se l'associazione di canale sottostante è basata su sessione. In questo caso viene usato un singolo canale per le chiamate al servizio. Tuttavia, se l'associazione di canale non è basata su sessione, il proxy del servizio crea un canale separato per ogni chiamata. Si noti, tuttavia, che i canali non basati su sessione vengono in pool e possono essere riutilizzati. Nel riutilizzo di un canale, il proxy del servizio mantiene aperto il canale se il canale sottostante non ha generato errori o se la chiamata su un canale ha generato un errore del proxy del servizio. Si noti che. tranne in caso di errore, una volta aperto, un canale viene mantenuto aperto finché il proxy del servizio è aperto e viene chiuso solo quando il proxy del servizio viene chiuso.


Se l'associazione di canale è basata su sessione e se il canale sottostante ha errori, la macchina a stati del proxy del servizio passa allo stato [**WS \_ SERVICE PROXY \_ STATE \_ \_ FAULTED.**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) Nel caso di un'associazione di canale non basata su sessione, un errore nel canale sottostante non causa la transizione del proxy allo stato **\_ \_ \_ \_ FAULTED del proxy WS SERVICE.**

Per altre informazioni sul proxy del servizio e sulla relativa relazione con lo stato, vedere [l'argomento Proxy del](service-proxy.md) servizio. Per esempi di associazioni di canale diverse, vedere gli esempi seguenti:

-   associazione di canali non di sessione, [HttpCalculatorClientExample](httpcalculatorclientexample.md)
-   associazione di canale basata su sessione, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)

 

 




