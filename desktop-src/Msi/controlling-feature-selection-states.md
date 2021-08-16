---
description: È possibile controllare le opzioni di installazione delle funzionalità disponibili per utenti e applicazioni da selezionare tramite la creazione della tabella Funzionalità e della tabella Componente.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Controllo degli stati di selezione delle caratteristiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd269e5b7b0c810df6f7f0909d56b98cdd1c54c9b51eacc40656fe48fc32f8e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379906"
---
# <a name="controlling-feature-selection-states"></a>Controllo degli stati di selezione delle caratteristiche

È possibile controllare le opzioni di installazione delle funzionalità disponibili per utenti e applicazioni da selezionare tramite la creazione della [tabella Delle](feature-table.md) funzionalità e della [tabella Componente](component-table.md).

-   Per impedire la selezione dello stato di annuncio per una funzionalità, includere **msidbFeatureAttributesDisallowAdvertise nel** campo Attributi della funzionalità nella [tabella Funzionalità](feature-table.md).
-   Per impedire la selezione degli stati run-from-source o run-from-network per una funzionalità, includere **msidbComponentAttributesLocalOnly** nei campi Attributi della tabella [Component](component-table.md) per ogni componente appartenente alla funzionalità. Se una funzionalità non include componenti, sono sempre disponibili le opzioni run-from-source ed run-from-my-computer.
-   Per impedire la selezione dello stato run-from-my-computer per una funzionalità, includere **msidbComponentAttributesSourceOnly** nei campi Attributi della tabella [Componente](component-table.md) per ogni componente appartenente alla funzionalità. Se una funzionalità non include componenti, sono sempre disponibili le opzioni run-from-source ed run-from-my-computer.
-   È possibile creare nuove funzionalità figlio includendo **msidbFeatureAttributesFollowParent** e **msidbFeatureAttributesUIDisallowAbsent nel** campo Attributi della tabella [Feature](feature-table.md).

 

 



