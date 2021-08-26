---
description: Tablet PC include la tecnologia per il riconoscimento dell'input penna più comunemente sotto forma di grafia.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Informazioni sul riconoscimento della grafia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4106d887eaa5bae2a162ab3c08a42c0d3b425b05a09b50bfcde626c05707f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884051"
---
# <a name="about-handwriting-recognition"></a>Informazioni sul riconoscimento della grafia

Tablet PC include la tecnologia per il riconoscimento dell'input penna più comunemente sotto forma di grafia. Il modulo software che fornisce il riconoscimento è detto riconoscimento. Un riconoscitore riconosce una lingua, un gruppo di lingue correlate o una classe di oggetti correlati, ad esempio note musicali, movimenti di sistema o forme geometriche. È possibile aggiungere in modo dinamico sistemi di riconoscimento al sistema di servizi input penna.

## <a name="recognition-steps"></a>Passaggi di riconoscimento

Il riconoscimento viene gestito tramite l'uso di un contesto di riconoscimento. Il riconoscimento è costituito da quattro passaggi di base:

1.  Impostazione dei vincoli di riconoscimento in base a:
    -   Selezione del riconoscitore e della modalità di input (vincoli geometrici).
    -   Impostazione dei vincoli di linguaggio. È ad esempio possibile limitare l'input ai caratteri alfanumerici oppure passare schemi per facilitare il riconoscimento.
2.  Invio dell'input penna al sistema di riconoscimento.
3.  Elaborazione dell'input (riconoscimento).
4.  Restituzione dei risultati del riconoscimento.

I passaggi 2 e 3 possono essere ripetuti in un ciclo oppure tutti i tratti input penna possono essere aggiunti all'input penna prima che venga tentato il riconoscimento.

## <a name="samples-and-related-topics"></a>Esempi e argomenti correlati

[L'esempio di riconoscimento](advanced-recognition-sample.md) avanzato illustra come usare i sistemi di riconoscimento con [**gli oggetti Ink**](inkdisp-class.md) per eseguire il riconoscimento dell'input penna.

[Il modello di esempio recognizer DLL](recognizer-dll-sample-template.md) contiene un modello per la creazione di una DLL di riconoscimento. Il modello contiene funzioni per la registrazione e l'annullamento della registrazione del server, nonché scheletri per le funzioni di riconoscimento primario.

Le sezioni seguenti descrivono i concetti di base alla base della tecnologia di riconoscimento tablet PC. Per informazioni dettagliate sulla creazione di riconoscitori personalizzati, vedere [Creazione di un riconoscitore.](creating-a-recognizer.md)

-   [Riconoscitori di testo](text-recognizers.md)
-   [Riconoscitori di oggetti](object-recognizers.md)
-   [Uso della raccolta Recognizers](using-the-recognizers-collection.md)
-   [Contesto del riconoscitore](recognizer-context.md)
-   [Segmenti di riconoscimento](recognition-segments.md)
-   [Riconoscimento del testo angolato](recognition-of-angled-text.md)
-   [Supporto del riordinamento dei tratti del riconoscitore](recognizer-stroke-reordering-support.md)
-   [Dizionari e factoid](dictionaries-and-factoids.md)
-   [Proprietà Confidence \[ Sul riconoscimento\]](confidence-property--about-recognition.md)
-   [Glifi alternativi](alternates.md)
-   [Segmenti e alternative di input penna](ink-segments-and-alternates.md)

 

 



