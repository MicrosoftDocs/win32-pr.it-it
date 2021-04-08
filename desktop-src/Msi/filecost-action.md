---
description: FileCostaction avvia le azioni di installazione standard di costingof dinamica.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Azione filecost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058387"
---
# <a name="filecost-action"></a>Azione filecost

Il FileCostaction avvia il [*costo*](c-gly.md)dinamico delle azioni di installazione standard.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Tutte le azioni standard o [personalizzate](custom-actions.md) che influiscono sui costi devono essere sequenziate prima dell'azione [CostInitialize](costinitialize-action.md) . Chiamare l'azione filecost immediatamente dopo l'azione CostInitialize. Chiamare quindi l'azione [CostFinalize secondo](costfinalize-action.md) dopo l'azione CostInitialize per rendere disponibili al programma di installazione tutti i calcoli dei costi finali tramite la tabella [Component](component-table.md) .

L'azione [CostInitialize](costinitialize-action.md) deve essere eseguita prima dell'azione filecost. Il programma di installazione determina quindi il costo dello spazio su disco di ogni file nella tabella dei [file](file-table.md) , in base ai singoli componenti (vedere la [tabella dei componenti](component-table.md)), accettando sia il clustering del [*volume*](v-gly.md) che la presenza di file esistenti che potrebbero dover essere sovrascritti. Verranno considerate anche tutte le azioni che utilizzano o rilasciano spazio su disco. Se viene trovato un file esistente, viene eseguito un controllo della versione del file per determinare se è effettivamente necessario installare il nuovo file. Se il numero di versione del file esistente è uguale o maggiore, il file esistente non viene sovrascritto e non è stato eseguito alcun costo dello spazio su disco. In tutti i casi, il programma di installazione utilizza i risultati del controllo del numero di versione per impostare lo stato di installazione di ogni file.

L'azione filecost Inizializza il calcolo dei costi con TheInstaller. Il [*costo*](c-gly.md) dinamico effettivo non si verifica finché non viene eseguita l'azione [CostFinalize secondo](costfinalize-action.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costo file](file-costing.md)
</dt> </dl>

 

 



