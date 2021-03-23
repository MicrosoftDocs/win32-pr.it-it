---
title: Heap del descrittore visibile dello shader
description: Gli heap del descrittore visibile dello shader sono heap di descrittori a cui possono fare riferimento gli shader tramite le tabelle dei descrittori.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104332"
---
# <a name="shader-visible-descriptor-heaps"></a>Heap del descrittore visibile dello shader

Gli heap del descrittore visibile dello shader sono heap di descrittori a cui possono fare riferimento gli shader tramite le tabelle dei descrittori.

-   [Overview](#overview)
-   [un esempio](#an-example)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Gli heap del descrittore a cui possono fare riferimento gli shader tramite le tabelle dei descrittori sono disponibili in un paio di varianti: un tipo di heap, D3D12 \_ SRV \_ UAV \_ CBV \_ descrittore \_ , può contenere visualizzazioni di risorse shader, viste di accesso non ordinate e visualizzazioni di buffer costanti, tutte intermiste. Qualsiasi posizione specificata nell'heap può essere uno dei tipi elencati dei descrittori. Un altro tipo di heap \_ , \_ Sampler di tipo heap del descrittore D3D12 \_ \_ , archivia solo i sampler, che riflettono il fatto che, per la maggior parte dell'hardware, i sampler vengono gestiti separatamente da SRVs, UAV, CBVs.

È possibile che gli heap dei descrittori di questi tipi siano visibili o meno dello shader quando l'heap viene creato (quest'ultimo non visibile, può essere utile per i descrittori di staging sulla CPU). Quando viene richiesto di essere visibile allo shader, ogni tipo di heap precedente potrebbe avere un limite di dimensioni hardware per ogni singola allocazione dell'heap del descrittore.

Le applicazioni possono creare un numero qualsiasi di heap di descrittori e gli heap dei descrittori non visibili per gli shader non sono limitati alle dimensioni. Se un heap del descrittore visibile dello shader creato dall'applicazione è inferiore al limite delle dimensioni hardware, il driver può scegliere di Sottoallocare l'heap del descrittore da un heap del descrittore sottostante più grande, in modo che più heap descrittore API rientrino in un heap descrittore hardware. Il motivo potrebbe essere che, per alcuni componenti hardware, il cambio tra gli heap del descrittore hardware durante l'esecuzione richiede che una GPU attenda inattiva (per assicurarsi che i riferimenti GPU all'heap del descrittore precedente siano finiti). Se tutti gli heap del descrittore creati da un'applicazione rientrano nelle capacità massime dell'heap hardware applicabile, non si verificheranno tali attese durante il cambio di heap del descrittore API durante il rendering. Le applicazioni devono tuttavia consentire la possibilità, tuttavia, che il cambio dell'heap del descrittore corrente possa comportare un'attesa di inattività.

Per evitare che questa operazione sia interessata da questa possibile attesa di inattività nel commutatore heap del descrittore, le applicazioni possono sfruttare le interruzioni del rendering che potrebbero influire sulla GPU per altri motivi, come il tempo necessario per eseguire le commutazioni dell'heap descrittore, dal momento che è in corso un'attesa per inattività

Il meccanismo e la semantica per l'identificazione degli heap dei descrittori per gli shader durante la registrazione dell'elenco di comandi/bundle sono descritti nella Guida di riferimento alle API.

## <a name="an-example"></a>un esempio

L'immagine seguente mostra due heap dei descrittori che fanno riferimento a due trame 2D separate archiviate in due slot di un heap predefinito di grandi dimensioni. L'heap del descrittore a cui è visibile lo shader può essere accessibile dalla pipeline grafica (inclusi gli shader), quindi la trama 2D è disponibile per la pipeline.

![heap di descrittori visibili e non visibili](images/descriptor-heaps.png)

> [!Note]  
> Spesso l'hardware GPU della quantità di memoria locale GPU scrivibile dalla CPU (definito memoria combinata) per gli heap dei descrittori è spesso limitato. Questo limite è in genere relativo a 96MB per tutti i processi. Un heap del descrittore del membro 1 milione, con descrittori 32byte, utilizzerebbe, ad esempio, 32 MB. Se necessario, il driver eseguirà il fallback sulla memoria di sistema, anche se è consigliabile non creare un numero elevato di heap descrittori di grandi dimensioni.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> </dl>

 

 




