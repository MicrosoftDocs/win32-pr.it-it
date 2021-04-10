---
description: Informazioni sul filtro di acquisizione audio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Informazioni sul filtro di acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125280"
---
# <a name="about-the-audio-capture-filter"></a>Informazioni sul filtro di acquisizione audio

DirectShow consente l'acquisizione dagli input analoghi in una scheda audio tramite il [filtro di acquisizione audio](audio-capture-filter.md). Questo filtro usa le API di WaveIn *xxx* per controllare qualsiasi dispositivo il cui driver supporta queste API. Ogni scheda del sistema è rappresentata da un'istanza separata del filtro.

Il filtro di acquisizione audio espone ogni input sulla scheda, ad esempio il microfono o l'input MIDI, come un pin di input. I pin di input rappresentano gli elementi esposti dal driver come righe di origine audio. Tuttavia, non vengono trasmessi dati attraverso questi pin di input e non si connettono ad altri filtri DirectShow. Forniscono semplicemente un modo per consentire a un'applicazione di controllare gli input. L'applicazione può usare un pin di input per abilitare o disabilitare l'input o per impostare le proprietà di combinazione, ad esempio la equalizzazione dei bassi, l'equalizzazione degli acuti, il Pan e così via. La quantità di controllo disponibile dipende dal driver. Per comprendere e sfruttare appieno le funzionalità di una scheda audio specifica, sarà necessaria la documentazione del produttore della scheda.

> [!Note]  
> È possibile acquisire dall'input di CD-Audio, ma questo flusso audio è già passato attraverso il convertitore da digitale a analogico, quindi si verifica una perdita di qualità del suono dal CD originale.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 



