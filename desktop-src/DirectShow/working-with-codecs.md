---
description: Uso dei codec
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Uso dei codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462a1340ef7e6a64aada586addcc73d95a993884fe2b026e74acde5fd286638c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650620"
---
# <a name="working-with-codecs"></a>Uso dei codec

Microsoft Windows diversi codec come componenti del sistema operativo. I codec disponibili includono sempre quelli forniti con qualsiasi versione di DirectX e Windows Media Player è stata inclusa nella Windows versione. È possibile installare codec aggiuntivi quando vengono installate versioni più recenti di DirectX o Windows Media Player o i runtime Windows Media SDK. Terze parti possono installare codec aggiuntivi in un sistema host; Questi codec possono essere progettati per funzionare solo con una particolare applicazione o possono supportare l'uso generale da parte di qualsiasi DirectShow applicazione.

I codec possono essere implementati in tre modi diversi:

-   Come codec installabile video per Windows audio o video di tipo video caricato da Gestione compressione video (VCM) o Gestione compressione audio (ACM). In generale, questa tecnologia è considerata deprecata e non è consigliabile usarla. I codec installabili partecipano ai DirectShow filtri tramite il filtro wrapper AVI Decompressor.
-   Come filtro DirectShow personalizzato. Molti codec di terze parti vengono implementati come filtri DirectShow nativi. Uno di questi filtri è il filtro decompressore MP3 Frauenhofer. In generale, questi filtri possono essere aggiunti al grafico dei filtri nei modi consueti. Un'eccezione a questa regola è che alcuni codec Windows Media™ Audio o Windows Media Video e il codec Microsoft MPEG-4 non possono essere aggiunti manualmente a un grafo di filtro. Questi filtri possono essere aggiunti solo dai filtri Lettore ASF e Writer ASF.
-   Come oggetti multimediali DirectX (DMO). Gli oggetti DMO sono il modo consigliato per implementare i codec perché possono essere usati all'interno di un grafico di filtro DirectShow usando il filtro wrapper DMO o in modo indipendente in qualsiasi altra applicazione di streaming non basata su DirectShow. Alcuni Windows video multimediali e Windows video multimediali vengono implementati come DMO. Come per i filtri Windows multimediali, questi DMO non possono essere usati all'esterno del contesto di Windows Media SDK. Ciò significa che in DirectShow possono essere aggiunti a un grafo solo tramite i filtri lettore ASF o ASF Writer.

In GraphEdit tutti questi diversi tipi di codec vengono visualizzati insieme nelle categorie seguenti:

-   Audio audio
-   Video a 360
-   DirectShow filtro

Molti di questi codec, tuttavia, vengono installati da terze parti o da altre applicazioni Microsoft o componenti del sistema operativo e non sono destinati all'uso da parte di DirectShow applicazioni. L'elenco dei codec visibili in GraphEdit dipende anche dalla versione di Windows in esecuzione nel sistema host e dalla versione di DirectShow SDK installata.

 

 



