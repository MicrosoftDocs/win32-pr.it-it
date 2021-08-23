---
title: Operazione OpenGL di base
description: Operazione OpenGL di base
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operazioni di base
- OpenGL, elaborazione dati
- OpenGL, fasi di elaborazione
- OpenGL, visualizzare elenchi
- elenchi di visualizzazione OpenGL
- OpenGL, analizzatori
- Analizzatori OpenGL
- Operazioni OpenGL, per vertice
- Operazioni per vertice OpenGL
- OpenGL, assembly primitivo
- Assembly primitivo OpenGL
- OpenGL, rasterizzazione
- rasterizzazione OpenGL
- OpenGL, operazioni per frammento
- Operazioni per frammento OpenGL
- framebuffers, operazioni di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72f6abed7d06a93985b798e72efbf4d6ec0901e7ad9fb4614f5bf81590cefcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554717"
---
# <a name="basic-opengl-operation"></a>Operazione OpenGL di base

Il diagramma seguente illustra come OpenGL elabora i dati. Come illustrato, i comandi entrano da sinistra e procedono attraverso una pipeline di elaborazione. Alcuni comandi specificano gli oggetti geometrici da disegnare e altri controllano la modalità di gestione degli oggetti durante varie fasi di elaborazione.

![Diagramma che mostra le fasi della pipeline di elaborazione dati OpenGL.](images/basic01.png)

Le fasi di elaborazione nell'operazione OpenGL di base sono le seguenti:

-   **Visualizzare l'elenco** Anziché fare in modo che tutti i comandi proceda immediatamente attraverso la pipeline, è possibile scegliere di accumulare alcuni di essi in un elenco di visualizzazione per l'elaborazione in un secondo momento.
-   **Analizzatore** La fase di elaborazione dell'analizzatore offre un modo efficiente per approssimare la geometria della curva e della superficie valutando i comandi polinomiali dei valori di input.
-   **Operazioni per vertice e assembly primitivo** OpenGL elabora primitivi geometricipoint, segmenti di linea e poligoni, tutti descritti dai vertici. I vertici vengono trasformati e accesi e le primitive vengono ritagliate nel viewport in preparazione alla rasterizzazione.
-   **Rasterizzazione** La fase di rasterizzazione produce una serie di indirizzi di buffer di frame e valori associati usando una descrizione bidimensionale di un punto, un segmento di linea o un poligono. Ogni frammento così prodotto viene inserito nell'ultima fase, per ogni frammento di operazioni.
-   **Operazioni per frammento** Si tratta delle operazioni finali eseguite sui dati prima che siano archiviati come pixel nel buffer frame.

    Le operazioni per frammento includono aggiornamenti condizionali di framebuffer in base ai valori z in ingresso e archiviati in precedenza (per il buffer z) e la fusione dei colori in pixel in ingresso con i colori archiviati, nonché la maschera e altre operazioni logiche sui valori in pixel.

I dati possono essere input sotto forma di pixel anziché di vertici. I dati sotto forma di pixel, ad esempio possono descrivere un'immagine da usare nel mapping della trama, ignorano la prima fase di elaborazione descritta in precedenza e vengono invece elaborati come pixel, nella fase delle operazioni pixel. Dopo le operazioni sui pixel, i dati pixel sono:

-   Archiviata come memoria della trama, da usare nella fase di rasterizzazione.
-   Rasterizzata, con i frammenti risultanti uniti nel buffer frame come se fossero stati generati da dati geometrici.

 

 




