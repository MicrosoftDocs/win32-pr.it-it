---
description: Informazioni sui dispositivi di acquisizione video
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Informazioni sui dispositivi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff3fff9f3d009006e300afdbe9986bfdc8d0a32ea618fdd2748efe0bd650b5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160184"
---
# <a name="about-video-capture-devices"></a>Informazioni sui dispositivi di acquisizione video

La maggior parte dei nuovi dispositivi di acquisizione video Windows driver WDM (Driver Model). Nell'architettura WDM, Microsoft fornisce un set di driver indipendenti dall'hardware, denominati driver di classe, e il fornitore dell'hardware fornisce minidriver specifici dell'hardware. Un minidriver implementa tutte le funzioni specifiche del dispositivo. Per la maggior parte delle funzioni, il minidriver chiama il driver di classe Microsoft.

In un DirectShow grafico dei filtri, qualsiasi dispositivo di acquisizione WDM viene visualizzato come filtro di acquisizione [video WDM.](wdm-video-capture-filter.md) Il filtro di acquisizione video WDM si configura in base alle caratteristiche del driver. Viene visualizzato sotto un nome specificato dal driver. Non verrà visualizzato un filtro denominato "WDM Video Capture Filter" in un punto qualsiasi del grafico.

Alcuni dispositivi di acquisizione meno recenti usano ancora i driver Video for Windows (VFW). Anche se questi driver sono ora obsoleti, sono supportati in DirectShow tramite il filtro [di acquisizione VFW.](vfw-capture-filter.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'acquisizione video in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



