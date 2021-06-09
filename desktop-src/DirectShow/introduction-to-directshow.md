---
description: Introduzione a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introduzione a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827225"
---
# <a name="introduction-to-directshow"></a>Introduzione a DirectShow

Microsoft® DirectShow® è un'architettura per lo streaming di contenuti multimediali nella piattaforma Microsoft Windows®. DirectShow consente l'acquisizione e la riproduzione di flussi multimediali di alta qualità. Supporta un'ampia gamma di formati, tra cui ASF (Advanced Systems Format), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) e file audio WAV. Supporta l'acquisizione da dispositivi digitali e analoghi basati su Windows Driver Model (WDM) o Video per Windows. Rileva e usa automaticamente l'hardware di accelerazione audio e video quando disponibile, ma supporta anche sistemi senza hardware di accelerazione.

DirectShow è basato sul Component Object Model (COM). Per scrivere un'applicazione o un componente DirectShow, è necessario comprendere la programmazione client COM. Per la maggior parte delle applicazioni, non è necessario implementare oggetti COM personalizzati. DirectShow fornisce i componenti necessari. Se tuttavia si vuole estendere DirectShow scrivendo componenti personalizzati, è necessario implementarli come oggetti COM.

DirectShow è progettato per C++. Microsoft non fornisce un'API gestita per DirectShow.

DirectShow semplifica le attività di riproduzione multimediale, conversione del formato e acquisizione. Allo stesso tempo, fornisce l'accesso all'architettura di controllo del flusso sottostante per le applicazioni che richiedono soluzioni personalizzate. È anche possibile creare componenti DirectShow personalizzati per supportare nuovi formati o effetti personalizzati.

Esempi di tipi di applicazione che è possibile scrivere con DirectShow includono lettori di file, lettori TV e DVD, applicazioni di modifica video, convertitori di formati di file, applicazioni di acquisizione audio-video, codificatori e decodificatori, processori di segnali digitali e altro ancora.

Questa sezione contiene i seguenti argomenti:

-   [Novità di DirectShow](whats-new-in-directshow.md)
-   [Formati supportati in DirectShow](supported-formats-in-directshow.md)
-   [Domande frequenti su DirectShow](directshow-faq.yml)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



