---
description: Simulazione Graph compilazione con GraphModifica
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulazione Graph compilazione con GraphModifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4f5bee201e2bd5b771348596b46caa513944aa148c7ec17a9e2974a360e60c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583197"
---
# <a name="simulating-graph-building-with-graphedit"></a>Simulazione Graph compilazione con GraphModifica

DirectShow fornisce un'utilità di debug denominata GraphEdit, che è possibile usare per creare e testare i grafici dei filtri.

GraphEdit è uno strumento visivo per la creazione di grafi di filtro. Con GraphEdit è possibile sperimentare con un grafo di filtro prima di scrivere qualsiasi codice dell'applicazione. È anche possibile caricare un grafo di filtro creato dall'applicazione per verificare che l'applicazione crei il grafico corretto. Se si sviluppa un filtro personalizzato, GraphEdit offre un modo rapido per testarlo: è sufficiente caricare un grafo con il filtro personalizzato e provare a eseguire il grafo. Se non si ha familiarità con DirectShow, GraphEdit è un buon modo per acquisire familiarità con i grafi di filtro e l'architettura DirectShow grafica.

La figura seguente mostra come GraphEdit rappresenta un semplice grafo di filtro.

![grafo di filtro semplice in graphedit](images/gedit09.png)

Ogni filtro è rappresentato come rettangolo. I quadrati più piccoli lungo i bordi dei filtri rappresentano i segnaposto. I pin di input sono sul lato sinistro del filtro e i pin di output sono sul lato destro. Le frecce rappresentano le connessioni tra i segnaposto.

Con GraphEdit è possibile:

-   Creare e modificare grafici di filtro usando un'interfaccia visiva con trascinamento della selezione.
-   Simulare chiamate a livello di codice per compilare un grafo.
-   Eseguire, sospendere, arrestare e cercare un grafo.
-   Visualizzare i filtri registrati nel computer e visualizzare le informazioni del Registro di sistema per ogni filtro.
-   Visualizzare le pagine delle proprietà dei filtri.
-   Visualizzare i tipi di supporti di connessioni pin.

Questa sezione contiene i seguenti argomenti:

-   [Uso di GraphModifica](using-graphedit.md)
-   [Caricamento di Graph da un processo esterno](loading-a-graph-from-an-external-process.md)
-   [Salvataggio di un filtro Graph in un grafoModifica file](saving-a-filter-graph-to-a-graphedit-file.md)
-   [Caricamento di un file GraphModifica file a livello di codice](loading-a-graphedit-file-programmatically.md)
-   [GraphModifica formato file](graphedit-file-format.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



