---
description: Oggetti multimediali DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Oggetti multimediali DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ef7dc17ab595748d9ccbfa16e33e7b4b8057d161c7f1e5d9f589e6768ec35f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821196"
---
# <a name="directx-media-objects"></a>Oggetti multimediali DirectX

> [!Note]  
> Gli oggetti DMO sono stati sostituiti da Media Foundation (MFT). [](/windows/desktop/medfound/media-foundation-transforms) Le DMO sono ancora supportate. Tuttavia, se si scrive un codec personalizzato o un plug-in di elaborazione audio/video, è consigliabile implementarlo come MFT.

 

DirectX Media Objects (DMO) sono componenti di streaming dei dati basati su COM. Per alcuni aspetti, gli oggetti DMO sono simili ai filtri DirectShow Microsoft. Analogamente DirectShow filtri, gli oggetti DMO accettano i dati di input e lo usano per produrre dati di output. Tuttavia, le API (Application Programming Interface) per dmo sono molto più semplici delle API corrispondenti per DirectShow. Di conseguenza, gli oggetti DMO sono più facili da creare, testare e usare. Gli oggetti DMO possono essere usati in molti scenari:

-   Le applicazioni basate DirectShow possono usare gli oggetti DMO tramite un DirectShow definito filtro [wrapper DMO.](dmo-wrapper-filter.md) La distinzione tra filtri e DMO è trasparente per l'applicazione. L'applicazione non chiama direttamente DMO API.
-   Le applicazioni basate su Microsoft DirectSound possono usare oggetti DMO con effetto audio. Anche in questo caso, l'applicazione è schermata dalle API DMO di basso livello dalle API DirectSound di livello superiore.
-   Le applicazioni possono usare direttamente gli oggetti DMO.

Pertanto, scrivendo un DMO, si crea un componente che può essere usato in un'ampia gamma di applicazioni. Questa documentazione contiene le sezioni seguenti:

-   [Informazioni sugli oggetti DMO](about-dmos.md)
-   [Uso di dmo](using-dmos.md)
-   [Scrittura di un DMO](writing-a-dmo.md)
-   [Parametri dei supporti](media-parameters.md)
-   [DMO Riferimento](dmo-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
