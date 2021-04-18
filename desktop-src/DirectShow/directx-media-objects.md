---
description: Oggetti multimediali DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Oggetti multimediali DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320456"
---
# <a name="directx-media-objects"></a>Oggetti multimediali DirectX

> [!Note]  
> DMOs sono stati sostituiti da [trasformazioni di Media Foundation](/windows/desktop/medfound/media-foundation-transforms) (MFTS). Le interfacce DMO sono ancora supportate. Tuttavia, se si scrive un codec personalizzato o un plug-in di elaborazione audio/video, è consigliabile implementarlo come MFT.

 

Gli oggetti multimediali DirectX (DMOs) sono componenti di streaming di dati basati su COM. Per alcuni aspetti, DMOs sono simili ai filtri Microsoft DirectShow. Analogamente ai filtri DirectShow, DMOs accetta i dati di input e li usa per produrre dati di output. Tuttavia, le API (Application Programming Interface) per DMOs sono molto più semplici delle API corrispondenti per DirectShow. Di conseguenza, DMOs sono più facili da creare, testare e usare. DMOs può essere usato in molti scenari:

-   Le applicazioni basate su DirectShow possono usare DMOs tramite un filtro DirectShow denominato filtro [wrapper DMO](dmo-wrapper-filter.md) . La distinzione tra Filters e DMOs è trasparente per l'applicazione. L'applicazione non chiama direttamente le API DMO.
-   Le applicazioni basate su Microsoft DirectSound possono usare l'effetto audio DMOs. Anche in questo caso, l'applicazione viene protetta dalle API DMO di basso livello dalle API DirectSound di livello superiore.
-   Le applicazioni possono usare direttamente DMOs.

Pertanto, scrivendo un DMO, viene creato un componente che può essere utilizzato in un'ampia gamma di applicazioni. Questa documentazione contiene le sezioni seguenti:

-   [Informazioni su DMOs](about-dmos.md)
-   [Uso di DMOs](using-dmos.md)
-   [Scrittura di un DMO](writing-a-dmo.md)
-   [Parametri dei supporti](media-parameters.md)
-   [Guida di riferimento a DMO](dmo-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
