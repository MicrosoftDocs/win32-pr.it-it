---
description: La determinazione dei costi è il processo di determinazione dei requisiti di spazio totale su disco per un'installazione.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Determinazione dei costi dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad2dc3ad9da4fab21345e74f3f9db99992445d7cf1e2266806bda55cd6ca638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529581"
---
# <a name="file-costing"></a>Determinazione dei costi dei file

La determinazione dei costi è il processo di determinazione dei requisiti di spazio totale su disco per un'installazione. Gli elementi calcolati nel processo di determinazione dei costi dei file includono la quantità di spazio su disco in cui i file vengono installati o rimossi, nonché la quantità di spazio su disco utilizzato dalle voci del Registro di sistema, dai collegamenti e da altri file esterni. I file esistenti che devono essere sovrascritti vengono calcolati anche nei totali dei costi del disco.

I costi totali vengono accumulati in base al componente e sono costituiti da tre parti separate: costi locali, costi di origine e costi di rimozione.[](components-and-features.md) Queste parti corrispondono al costo del disco che si verifica se il componente viene installato in locale, installato per l'esecuzione dal supporto di origine o rimosso.

Tutti i calcoli che comportano il costo di installazione dei file dipendono dal volume del disco in cui il file deve essere installato o rimosso. Ogni volta che la directory associata a un componente cambia, i costi dei file di installazione controllati da tale componente devono essere ricalcolati. Ad esempio, poiché una modifica della directory potrebbe implicare anche una modifica del volume, le dimensioni dei file in cluster devono essere ricalcolate. Inoltre, è necessario controllare la nuova directory per determinare se è necessario prendere in considerazione eventuali file esistenti che possono essere sovrascritti.

Dopo aver [chiamato l'azione CostInitialize,](costinitialize-action.md) è [necessario chiamare l'azione FileCost.](filecost-action.md) L'azione CostInitialize inizializza le routine interne del programma di installazione che calcolano in modo dinamico i costi del disco coinvolti nelle azioni di installazione standard. A questo punto non viene eseguito alcun altro calcolo dei costi dinamici.

Successivamente, è [necessario chiamare l'azione CostFinalize.](costfinalize-action.md) Questa azione finalizza tutti i calcoli dei costi e rende disponibili i dati di determinazione costi tramite la [tabella](component-table.md) Componente.

Al termine dell'esecuzione dell'azione [CostFinalize,](costfinalize-action.md) la tabella [Component](component-table.md) viene completamente inizializzata e, se necessario, può essere avviata una sequenza di finestre di dialogo dell'interfaccia utente contenente un controllo [SelectionTree.](selectiontree-control.md) Le finestre di dialogo dell'interfaccia utente possono offrire all'utente [](feature-table.md) la possibilità di modificare lo stato di selezione o la directory di destinazione di qualsiasi funzionalità nella tabella Funzionalità. Il processo è simile quando lo stato di selezione di un componente cambia; In questo caso, tuttavia, viene ricalcolato solo il costo dinamico del componente modificato.

Dopo che l'utente ha completato la selezione delle funzionalità nell'interfaccia utente, [deve essere chiamata l'azione InstallValidate.](installvalidate-action.md) Questa azione verifica che tutti i volumi a cui è stato attribuito il costo dispongano di spazio sufficiente per l'installazione.

 

 



