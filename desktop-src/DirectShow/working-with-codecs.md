---
description: Uso dei codec
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Uso dei codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308939"
---
# <a name="working-with-codecs"></a>Uso dei codec

Microsoft Windows fornisce diversi codec come componenti del sistema operativo. I codec disponibili includono sempre quelli forniti con la versione di DirectX e Windows Media Player inclusa nella versione di Windows. È possibile installare codec aggiuntivi quando si installano versioni più recenti di DirectX o Windows Media Player o i runtime di Windows Media SDK. Le terze parti possono installare codec aggiuntivi in un sistema host; Questi codec possono essere progettati per funzionare solo con una particolare applicazione oppure possono supportare l'utilizzo generale da qualsiasi applicazione DirectShow.

I codec possono essere implementati in tre modi diversi:

-   Come video per il codec di tipo Windows audio o video installabile caricato da video Compression Manager (VCM) o Audio Compression Manager (ACM). In generale, questa tecnologia è considerata deprecata e non è consigliabile usarla. I codec installabili partecipano ai grafici filtro DirectShow tramite il filtro wrapper di decompressione AVI.
-   Come filtro DirectShow. Molti codec di terze parti vengono implementati come filtri DirectShow nativi. Un filtro di questo tipo è il filtro Decompressore Frauenhofer MP3. In generale, questi filtri possono essere aggiunti al grafico di filtro nei modi usuali. Un'eccezione a questa regola è rappresentata dal non è possibile aggiungere manualmente alcuni codec audio o Windows Media Video di Windows Media™ e il codec Microsoft MPEG-4 a un grafico di filtro. Questi filtri possono essere aggiunti solo dai filtri ASF Reader e writer ASF.
-   Come DirectX Media Objects (DMOs). DMOs è il metodo consigliato per implementare i codec, in quanto possono essere usati all'interno di un grafico del filtro DirectShow usando il filtro del wrapper DMO oppure indipendentemente da qualsiasi altra applicazione di streaming non basata su DirectShow. Alcuni Windows Media Audio e Windows Media Video codec sono implementati come DMOs. Come per i filtri Windows Media, questi DMOs non possono essere usati al di fuori del contesto di Windows Media SDK. Ciò significa che in DirectShow possono essere aggiunti solo a un grafico tramite i filtri ASF Reader o writer ASF.

In GraphEdit tutti questi diversi tipi di codec vengono visualizzati insieme nelle categorie seguenti:

-   Compressore audio
-   Compressore video
-   Filtro DirectShow

Molti di questi codec, tuttavia, vengono installati da terze parti o da altre applicazioni Microsoft o componenti del sistema operativo e non sono destinati all'utilizzo da parte di altre applicazioni DirectShow. L'elenco di codec visibile in GraphEdit dipende anche dalla versione di Windows in esecuzione nel sistema host e dalla versione di DirectShow SDK installata.

 

 



