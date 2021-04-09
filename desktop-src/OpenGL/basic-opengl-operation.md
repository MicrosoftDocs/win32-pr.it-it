---
title: Operazione OpenGL di base
description: Operazione OpenGL di base
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operazioni di base
- OpenGL, elaborazione dati
- OpenGL, fasi di elaborazione
- OpenGL, elenchi di visualizzazione
- visualizzazione degli elenchi OpenGL
- OpenGL, analizzatori
- analizzatori OpenGL
- Operazioni di OpenGL, per vertice
- operazioni per vertice OpenGL
- OpenGL, assembly primitivo
- OpenGL assembly primitivo
- OpenGL, rasterizzazione
- rasterizzazione OpenGL
- Operazioni OpenGL, per frammento
- operazioni per frammenti OpenGL
- framebuffer, operazioni di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968824"
---
# <a name="basic-opengl-operation"></a>Operazione OpenGL di base

Il diagramma seguente illustra il modo in cui OpenGL elabora i dati. Come illustrato, i comandi entrano da sinistra e passano attraverso una pipeline di elaborazione. Alcuni comandi specificano oggetti geometrici da disegnare e altri controllano il modo in cui gli oggetti vengono gestiti durante le varie fasi di elaborazione.

![Diagramma che illustra le fasi della pipeline di elaborazione dati OpenGL.](images/basic01.png)

Le fasi di elaborazione nell'operazione OpenGL di base sono le seguenti:

-   **Elenco di visualizzazione** Anziché fare in modo che tutti i comandi procedano immediatamente attraverso la pipeline, è possibile scegliere di accumularne alcuni in un elenco di visualizzazione per l'elaborazione in un secondo momento.
-   **Analizzatore** La fase di elaborazione dell'analizzatore fornisce un modo efficiente per approssimare la geometria della curva e della superficie valutando i comandi polinomiali dei valori di input.
-   **Operazioni per vertice e assembly primitivo** OpenGL elabora i primitivespoints geometrici, i segmenti di linea e polygonsall di cui sono descritti i vertici. I vertici vengono trasformati e illuminati e le primitive vengono ritagliate nel viewport in preparazione per la rasterizzazione.
-   **Rasterizzazione** La fase di rasterizzazione produce una serie di indirizzi del buffer dei frame e valori associati usando una descrizione bidimensionale di un punto, un segmento di linea o un poligono. Ogni frammento generato viene inserito nell'ultima fase, ovvero le operazioni per frammento.
-   **Operazioni per frammento** Queste sono le operazioni finali eseguite sui dati prima di essere archiviate come pixel nel framebuffer.

    Le operazioni per frammento includono gli aggiornamenti condizionali per il framebuffer in base ai valori z in ingresso e archiviati in precedenza (per il buffering z) e la combinazione dei colori dei pixel in ingresso con i colori archiviati, nonché la maschera e altre operazioni logiche sui valori dei pixel.

I dati possono essere di input in formato pixel anziché vertici. I dati sotto forma di pixel, ad esempio, possono descrivere un'immagine da usare nel mapping di trama, ignora la prima fase di elaborazione descritta sopra e viene invece elaborata come pixel nella fase operazioni pixel. Di seguito sono riportate le operazioni pixel, ovvero i dati pixel:

-   Archiviato come memoria di trama, da utilizzare nella fase di rasterizzazione.
-   Rasterizzato, con i frammenti risultanti Uniti nel framebuffer esattamente come se fossero stati generati da dati geometrici.

 

 




