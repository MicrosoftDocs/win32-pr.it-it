---
description: Informazioni sull'API Transcode
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Informazioni sull'API Transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca7a5c39ebb4527a615c4c488239a1da4b88283f66199d25f6613a8d1f9bd82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449776"
---
# <a name="about-the-transcode-api"></a>Informazioni sull'API Transcode

Il diagramma seguente illustra in che modo l'API di transcodifica è correlata al resto della pipeline Media Foundation codifica.

![diagramma che mostra l'API transcodifica.](images/encoding08.png)

La pipeline di codifica contiene gli oggetti di elaborazione dati seguenti:

-   Origine multimediale
-   Decodificatore
-   Ridimensionatore video o resampler audio
-   Codificatore
-   Sink multimediale

Il ridimensionamento video è necessario solo se le dimensioni del video di output sono diverse dall'origine. Il resampler audio è necessario solo se l'audio deve essere ricampionato prima della codifica. La coppia decodificatore/codificatore è necessaria per la transcoding, ma non per il remuxing.

La topologia *di codifica* è il set di oggetti pipeline (origine, decodificatore, ridimensionatore, resampler, codificatore e sink multimediale), oltre ai punti di connessione tra di essi. Per altre informazioni sulle topologie, vedere [Topologie.](topologies.md)

Componenti diversi sono responsabili della creazione dei vari oggetti pipeline:

-   L'applicazione usa in genere il [resolver di origine](source-resolver.md) per creare l'origine multimediale.
-   La [sessione multimediale](media-session.md) carica e configura il decodificatore, il ridimensionatore video e il resampler audio. Internamente, usa il caricatore della topologia per eseguire questa operazione (vedere [**IMFTopoLoader).**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
-   L'API di transcodifica carica e configura il codificatore e il sink multimediale.

Le applicazioni avanzate possono configurare direttamente il codificatore e il sink multimediale, anziché usare l'API di transcodifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[Uso dell'API Transcode](fast-transcode-objects.md)
</dt> </dl>

 

 



