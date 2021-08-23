---
title: Heap dei descrittori visibili allo shader
description: Gli heap dei descrittori visibili allo shader sono heap di descrittori a cui gli shader possono fare riferimento tramite tabelle di descrittori.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96fbbb37f3337912780e5882918c0fcbc146c41f8dc60ddf3ba5d2a35c82c1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045394"
---
# <a name="shader-visible-descriptor-heaps"></a>Heap dei descrittori visibili allo shader

Gli heap dei descrittori visibili allo shader sono heap di descrittori a cui gli shader possono fare riferimento tramite tabelle di descrittori.

-   [Overview](#overview)
-   [un esempio](#an-example)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Gli heap dei descrittori a cui gli shader possono fare riferimento tramite le tabelle dei descrittori sono disponibili in un paio di tipi: un tipo di heap, D3D12 SRV UAV DESCRIPTOR HEAP, può contenere visualizzazioni di risorse shader, viste di accesso non ordinate e visualizzazioni buffer costanti, tutte \_ \_ \_ \_ \_ intermixate. Qualsiasi posizione specificata nell'heap può essere uno qualsiasi dei tipi elencati di descrittori. Un altro tipo di heap, D3D12 DESCRIPTOR HEAP TYPE SAMPLER, archivia solo i campionatori, riflettendo il fatto che per la maggior parte dell'hardware, i campionatori vengono gestiti separatamente da \_ \_ \_ \_ SRV, UAV e CBV.

È possibile che gli heap dei descrittori di questi tipi siano visibili o meno allo shader quando viene creato l'heap (quest'ultimo, non visibile allo shader, può essere utile per i descrittori di staging nella CPU). Quando viene richiesto che lo shader sia visibile, ognuno dei tipi di heap precedenti può avere un limite di dimensioni hardware per qualsiasi allocazione dell'heap dei singoli descrittori.

Le applicazioni possono creare un numero qualsiasi di heap dei descrittori e le dimensioni degli heap dei descrittori non visibili allo shader non sono vincolate. Se un heap del descrittore visibile allo shader creato dall'applicazione è inferiore al limite di dimensioni hardware, il driver può scegliere di sottoallocare l'heap del descrittore da un heap descrittore sottostante più grande in modo che più heap del descrittore API si adattino all'interno di un heap descrittore hardware. Ciò può verificarsi perché per alcuni componenti hardware, il passaggio tra gli heap dei descrittori hardware durante l'esecuzione richiede un'attesa GPU per inattività (per garantire che i riferimenti GPU all'heap descrittore precedente siano stati completati). Se tutti gli heap dei descrittori creati da un'applicazione rientrano nelle capacità massime dell'heap hardware applicabile, non si verificheranno attese di questo tipo quando si cambia heap dei descrittori API durante il rendering. Le applicazioni devono consentire la possibilità, tuttavia, che il cambio dell'heap del descrittore corrente possa causare un'attesa di inattività.

Per evitare di essere influenzati da questa possibile attesa di inattività sull'opzione dell'heap dei descrittori, le applicazioni possono sfruttare le interruzioni del rendering che potrebbero causare l'inattività della GPU per altri motivi, in quanto il tempo necessario per eseguire le opzioni dell'heap dei descrittori, poiché è comunque in corso un'attesa di inattività.

Il meccanismo e la semantica per l'identificazione degli heap dei descrittori negli shader durante la registrazione di elenchi di comandi/bundle sono descritti nelle informazioni di riferimento sulle API.

## <a name="an-example"></a>un esempio

L'immagine seguente mostra due heap di descrittori che fanno riferimento a due trame 2D separate archiviate in due slot di un heap predefinito di grandi dimensioni. L'heap del descrittore visibile allo shader è accessibile dalla pipeline grafica (inclusi gli shader) e di conseguenza la trama 2D è disponibile per la pipeline.

![heap dei descrittori visibili e non visibili](images/descriptor-heaps.png)

> [!Note]  
> È spesso previsto un limite per l'hardware GPU della quantità di memoria locale GPU scrivibile dalla CPU (detta memoria combinata di scrittura) per gli heap dei descrittori. In genere questo limite è di circa 96 MB per tutti i processi. Un heap descrittore di un milione di membri, con descrittori di 32byte, ad esempio, userebbe fino a 32 MB. Il driver eseguirerà il fall back nella memoria di sistema, se necessario, anche se è consigliabile non creare un numero elevato di heap dei descrittori di grandi dimensioni.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap dei descrittori](descriptor-heaps.md)
</dt> </dl>

 

 




