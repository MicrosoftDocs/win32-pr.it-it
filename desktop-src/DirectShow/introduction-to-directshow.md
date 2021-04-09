---
description: Introduzione a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introduzione a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124353"
---
# <a name="introduction-to-directshow"></a>Introduzione a DirectShow

Microsoft® DirectShow® è un'architettura per lo streaming di contenuti multimediali sulla piattaforma® di Microsoft Windows. DirectShow fornisce l'acquisizione e la riproduzione di alta qualità dei flussi multimediali. Supporta un'ampia gamma di formati, tra cui il formato ASF (Advanced Systems Format), MPEG (Motion Picture Experts Group), Audio-Video file con interfoliazione (AVI), MPEG Audio Layer-3 (MP3) e WAV audio. Supporta l'acquisizione da dispositivi digitali e analoghi basati sul Windows Driver Model (WDM) o sul video per Windows. Rileva automaticamente e utilizza hardware di accelerazione video e audio, se disponibile, ma supporta anche sistemi senza hardware di accelerazione.

DirectShow si basa sul Component Object Model (COM). Per scrivere un'applicazione o un componente DirectShow, è necessario comprendere la programmazione client COM. Per la maggior parte delle applicazioni, non è necessario implementare oggetti COM personalizzati. DirectShow fornisce i componenti necessari. Se si desidera estendere DirectShow scrivendo i propri componenti, è tuttavia necessario implementarli come oggetti COM.

DirectShow è progettato per C++. Microsoft non fornisce un'API gestita per DirectShow.

DirectShow semplifica la riproduzione dei contenuti multimediali, la conversione del formato e le attività di acquisizione. Allo stesso tempo, fornisce l'accesso all'architettura di controllo del flusso sottostante per le applicazioni che richiedono soluzioni personalizzate. È anche possibile creare componenti DirectShow personalizzati per supportare nuovi formati o effetti personalizzati.

Esempi di tipi di applicazione che è possibile scrivere con DirectShow includono lettori di file, lettori TV e DVD, applicazioni di modifica video, convertitori di formati di file, applicazioni di acquisizione video audio, codificatori e decodificatori, processori di segnali digitali e molto altro.

Questa sezione contiene i seguenti argomenti:

-   [Novità di DirectShow](whats-new-in-directshow.md)
-   [Formati supportati in DirectShow](supported-formats-in-directshow.md)
-   [Domande frequenti su DirectShow](directshow-faq.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



