---
description: Introduzione a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introduzione a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cd4dc2a75233c519c4ca3d5db213451b097c0528ab782109da611b6e35aca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952580"
---
# <a name="introduction-to-directshow"></a>Introduzione a DirectShow

Microsoft® DirectShow® è un'architettura per lo streaming di contenuti multimediali nella piattaforma Windows® Microsoft. DirectShow consente l'acquisizione e la riproduzione di flussi multimediali di alta qualità. Supporta un'ampia gamma di formati, tra cui ASF (Advanced Systems Format), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) e file audio WAV. Supporta l'acquisizione da dispositivi digitali e analoghi basati su Windows Driver Model (WDM) o Video per Windows. Rileva e usa automaticamente l'hardware di accelerazione audio e video quando disponibile, ma supporta anche sistemi senza hardware di accelerazione.

DirectShow è basato sul Component Object Model (COM). Per scrivere un'DirectShow o un componente, è necessario comprendere la programmazione client COM. Per la maggior parte delle applicazioni, non è necessario implementare oggetti COM personalizzati. DirectShow fornisce i componenti necessari. Se tuttavia si desidera estendere DirectShow mediante la scrittura di componenti personalizzati, è necessario implementarli come oggetti COM.

DirectShow è progettato per C++. Microsoft non fornisce un'API gestita per DirectShow.

DirectShow semplifica la riproduzione multimediale, la conversione del formato e le attività di acquisizione. Allo stesso tempo, fornisce l'accesso all'architettura di controllo del flusso sottostante per le applicazioni che richiedono soluzioni personalizzate. È anche possibile creare componenti personalizzati DirectShow per supportare nuovi formati o effetti personalizzati.

Esempi di tipi di applicazioni che è possibile scrivere con DirectShow includono lettori di file, lettori TV e DVD, applicazioni di modifica video, convertitori di formati di file, applicazioni di acquisizione audio-video, codificatori e decodificatori, processori di segnali digitali e altro ancora.

Questa sezione contiene i seguenti argomenti:

-   [Novità di DirectShow](whats-new-in-directshow.md)
-   [Formati supportati in DirectShow](supported-formats-in-directshow.md)
-   [DirectShow Domande frequenti](directshow-faq.yml)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



