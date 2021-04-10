---
description: Argomenti sull'acquisizione avanzata
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Argomenti sull'acquisizione avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125067"
---
# <a name="advanced-capture-topics"></a>Argomenti sull'acquisizione avanzata

Questa sezione descrive alcuni aspetti avanzati dell'acquisizione video in DirectShow. La maggior parte dei problemi descritti in questa sezione viene gestita automaticamente dall'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Tuttavia, le informazioni potrebbero essere utili se è necessario risolvere i problemi relativi a un'applicazione di acquisizione video. È inoltre consigliabile leggere questa sezione se l'applicazione compila un grafico di acquisizione personalizzato di un certo tipo e si ritiene che ICaptureGraphBuilder2 non soddisfi le proprie esigenze. Infine, in questa sezione vengono fornite alcune informazioni sull'utilizzo del filtro VMR (video Mixing Renderer) in un'applicazione di acquisizione video.

È possibile creare un grafico di acquisizione video completamente usando i metodi [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . È anche possibile combinare le due interfacce, usando ICaptureGraphBuilder2 per alcune attività e IGraphBuilder per altri.

Questa sezione contiene i seguenti argomenti:

-   [Gestione degli eventi di ridisegno in acquisizione video](handling-repaint-events-in-video-capture.md)
-   [Utilizzo delle categorie pin](working-with-pin-categories.md)
-   [Uso del filtro Smart Tee](using-the-smart-tee-filter.md)
-   [Uso del mixer overlay in acquisizione video](using-the-overlay-mixer-in-video-capture.md)
-   [PIN della porta video](video-port-pins.md)
-   [Tipo di formato VideoInfo2](videoinfo2-format-type.md)
-   [Creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md)
-   [Filtri driver di classe WDM](wdm-class-driver-filters.md)
-   [Uso di WDDM Capture in DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



