---
description: È possibile controllare quali opzioni di installazione delle funzionalità sono disponibili per gli utenti e le applicazioni da selezionare creando la tabella delle funzionalità e la tabella dei componenti.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Controllo degli Stati di selezione delle funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233708"
---
# <a name="controlling-feature-selection-states"></a>Controllo degli Stati di selezione delle funzionalità

È possibile controllare quali opzioni di installazione delle funzionalità sono disponibili per gli utenti e le applicazioni da selezionare creando la [tabella delle funzionalità](feature-table.md) e la [tabella dei componenti](component-table.md).

-   Per evitare la selezione dello stato di annuncio per una funzionalità, includere **msidbFeatureAttributesDisallowAdvertise** nel campo attributi della funzionalità della [tabella delle funzionalità](feature-table.md).
-   Per evitare la selezione degli Stati di esecuzione dall'origine o della rete per una funzionalità, includere **msidbComponentAttributesLocalOnly** nei campi degli attributi della [tabella dei componenti](component-table.md) per ogni componente appartenente alla funzionalità. Se una funzionalità non dispone di componenti, per la funzionalità sono sempre disponibili le opzioni Esegui da origine e esecuzione da computer.
-   Per evitare la selezione dello stato di esecuzione dal computer per una funzionalità, includere **msidbComponentAttributesSourceOnly** nei campi degli attributi della [tabella dei componenti](component-table.md) per ogni componente appartenente alla funzionalità. Se una funzionalità non dispone di componenti, per la funzionalità sono sempre disponibili le opzioni Esegui da origine e esecuzione da computer.
-   È possibile creare nuove funzionalità figlio includendo **msidbFeatureAttributesFollowParent** e **MsidbFeatureAttributesUIDisallowAbsent** nel campo Attributes della [tabella Feature](feature-table.md).

 

 



