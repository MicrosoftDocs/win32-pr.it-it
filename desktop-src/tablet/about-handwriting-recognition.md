---
description: Tablet PC include la tecnologia per il riconoscimento dell'input penna più comunemente sotto forma di grafia.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Informazioni sul riconoscimento della grafia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319578"
---
# <a name="about-handwriting-recognition"></a>Informazioni sul riconoscimento della grafia

Tablet PC include la tecnologia per il riconoscimento dell'input penna più comunemente sotto forma di grafia. Il modulo software che fornisce il riconoscimento è denominato riconoscimento. Un riconoscimento riconosce una lingua, un gruppo di linguaggi correlati o una classe di oggetti correlati, ad esempio note musicali, movimenti di sistema o forme geometriche. È possibile aggiungere in modo dinamico i riconoscitori al sistema dei servizi Ink.

## <a name="recognition-steps"></a>Procedura di riconoscimento

Il riconoscimento viene gestito tramite l'utilizzo di un contesto di riconoscimento. Il riconoscimento è costituito da quattro passaggi di base:

1.  Configurazione dei vincoli di riconoscimento:
    -   Selezione del riconoscimento e della modalità di input (vincoli geometrici).
    -   Impostazione dei vincoli della lingua. Ad esempio, è possibile limitare l'input ai caratteri alfanumerici oppure è possibile passare gli schemi per facilitare il riconoscimento.
2.  Invio dell'input penna al riconoscimento.
3.  Elaborazione dell'input (riconoscimento).
4.  Restituzione dei risultati del riconoscimento.

I passaggi 2 e 3 possono essere ripetuti in un ciclo oppure tutti i tratti di input penna possono essere aggiunti all'input penna prima del tentativo di riconoscimento.

## <a name="samples-and-related-topics"></a>Esempi e argomenti correlati

Nell' [esempio Advanced Recognition](advanced-recognition-sample.md) viene illustrato come utilizzare i riconoscitori con oggetti [**Ink**](inkdisp-class.md) per eseguire il riconoscimento dell'input penna.

Il [modello di esempio della DLL di riconoscimento](recognizer-dll-sample-template.md) contiene un modello per la creazione di una dll del riconoscitore. Il modello contiene funzioni per la registrazione e l'annullamento della registrazione del server, nonché scheletri per le funzioni di riconoscimento primarie.

Nelle sezioni seguenti vengono descritti i concetti di base della tecnologia di riconoscimento dei Tablet PC. Per informazioni dettagliate sulla creazione di riconoscitori personalizzati, vedere [creazione di un riconoscimento](creating-a-recognizer.md).

-   [Riconoscitori di testo](text-recognizers.md)
-   [Riconoscitori di oggetti](object-recognizers.md)
-   [Uso della raccolta Recognizers](using-the-recognizers-collection.md)
-   [Contesto di riconoscimento](recognizer-context.md)
-   [Segmenti di riconoscimento](recognition-segments.md)
-   [Riconoscimento del testo angolato](recognition-of-angled-text.md)
-   [Supporto per il riordinamento del tratto del riconoscimento](recognizer-stroke-reordering-support.md)
-   [Dizionari e factoids](dictionaries-and-factoids.md)
-   [Proprietà confidenza \[ sul riconoscimento\]](confidence-property--about-recognition.md)
-   [Glifi alternativi](alternates.md)
-   [Segmenti di input penna e alternative](ink-segments-and-alternates.md)

 

 



