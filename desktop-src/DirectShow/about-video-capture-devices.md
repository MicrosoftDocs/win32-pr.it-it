---
description: Informazioni sui dispositivi di acquisizione video
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Informazioni sui dispositivi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746375"
---
# <a name="about-video-capture-devices"></a>Informazioni sui dispositivi di acquisizione video

La maggior parte dei nuovi dispositivi di acquisizione video usa i driver Windows Driver Model (WDM). Nell'architettura WDM Microsoft fornisce un set di driver indipendenti dall'hardware, detti driver di classe, e il fornitore dell'hardware fornisce i minidriver specifici dell'hardware. Un minidriver implementa tutte le funzioni specifiche del dispositivo. per la maggior parte delle funzioni, minidriver chiama il driver di classe Microsoft.

In un grafico di filtro DirectShow, qualsiasi dispositivo di acquisizione WDM viene visualizzato come filtro di [acquisizione video WDM](wdm-video-capture-filter.md) . Il filtro di acquisizione video WDM si configura in base alle caratteristiche del driver. Viene visualizzato con un nome fornito dal driver. non verrà visualizzato un filtro denominato "Filtro acquisizione video WDM" in qualsiasi punto del grafico.

Alcuni dispositivi di acquisizione precedenti utilizzano ancora driver video for Windows (VFW). Sebbene questi driver siano obsoleti, sono supportati in DirectShow tramite il filtro di [acquisizione VFW](vfw-capture-filter.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su acquisizione video in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



