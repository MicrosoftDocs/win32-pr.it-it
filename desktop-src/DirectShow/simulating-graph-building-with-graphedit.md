---
description: Simulazione della creazione di grafici con GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulazione della creazione di grafici con GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481965"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simulazione della creazione di grafici con GraphEdit

DirectShow fornisce un'utilità di debug denominata GraphEdit, che è possibile utilizzare per creare e testare i grafici dei filtri.

GraphEdit è uno strumento visivo per la creazione di grafici di filtro. Con GraphEdit è possibile sperimentare un grafico di filtro prima di scrivere il codice dell'applicazione. È anche possibile caricare un grafico di filtro creato dall'applicazione per verificare che l'applicazione stia creando il grafo corretto. Se si sviluppa un filtro personalizzato, GraphEdit offre un modo rapido per testarlo: è sufficiente caricare un grafo con il filtro personalizzato e provare a eseguire il grafo. Se non si ha familiarità con DirectShow, GraphEdit è un modo efficace per acquisire familiarità con i grafici di filtro e l'architettura DirectShow.

Nella figura seguente viene illustrato come GraphEdit rappresenta un semplice grafico a filtro.

![grafico a filtro semplice in GraphEdit](images/gedit09.png)

Ogni filtro è rappresentato come rettangolo. I quadrati più piccoli lungo i bordi dei filtri rappresentano i pin. I pin di input si trovano sul lato sinistro del filtro e i pin di output si trovano sul lato destro. Le frecce rappresentano le connessioni tra i pin.

Con GraphEdit è possibile:

-   Creare e modificare i grafici di filtro usando un'interfaccia visiva, con trascinamento della selezione.
-   Simula le chiamate a livello di codice per la compilazione di un grafico.
-   Eseguire, sospendere, arrestare e cercare un grafo.
-   Vedere quali filtri sono registrati nel computer e visualizzare le informazioni del registro di sistema per ogni filtro.
-   Visualizzare le pagine delle proprietà del filtro.
-   Visualizzare i tipi di supporto delle connessioni pin.

Questa sezione contiene i seguenti argomenti:

-   [Uso di GraphEdit](using-graphedit.md)
-   [Caricamento di un grafico da un processo esterno](loading-a-graph-from-an-external-process.md)
-   [Salvataggio di un grafico di filtro in un file GraphEdit](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Caricamento di un file GraphEdit a livello di codice](loading-a-graphedit-file-programmatically.md)
-   [Formato di file GraphEdit](graphedit-file-format.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



