---
description: Informazioni sull'API transcodifica
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Informazioni sull'API transcodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560746"
---
# <a name="about-the-transcode-api"></a>Informazioni sull'API transcodifica

Il diagramma seguente illustra il modo in cui l'API transcode è correlata al resto della pipeline di codifica Media Foundation.

![diagramma che mostra l'API transcodifica.](images/encoding08.png)

La pipeline di codifica contiene gli oggetti di elaborazione dati seguenti:

-   Origine supporto
-   Decodificatore
-   Video Resizer o ricampionatore audio
-   Codificatore
-   Sink multimediale

Il video Resizer è necessario solo se le dimensioni del video di output sono diverse dall'origine. Il ricampionatore audio è necessario solo se l'audio deve essere ricampionato prima della codifica. La coppia Decodificatore/codificatore è necessaria per la transcodifica, ma non per remuxing.

La *topologia* di codifica è il set di oggetti pipeline (origine, decodificatore, Resizer, Resampler, codificatore e sink multimediale), più i punti di connessione tra di essi. Per ulteriori informazioni sulle topologie, vedere [topologie](topologies.md).

Componenti diversi sono responsabili della creazione dei vari oggetti pipeline:

-   L'applicazione usa in genere il [resolver di origine](source-resolver.md) per creare l'origine multimediale.
-   La [sessione multimediale](media-session.md) carica e configura il decodificatore, il ridimensionamento video e il ricampionatore audio. Internamente, usa il caricatore della topologia a tale scopo (vedere [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).
-   L'API transcode carica e configura il codificatore e il sink multimediale.

Le applicazioni avanzate possono configurare direttamente il codificatore e il sink multimediale, anziché usare l'API transcode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API transcodifica](transcode-api.md)
</dt> <dt>

[Uso dell'API transcode](fast-transcode-objects.md)
</dt> </dl>

 

 



