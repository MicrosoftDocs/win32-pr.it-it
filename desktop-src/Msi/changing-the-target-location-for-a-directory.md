---
description: Se possibile, il modo migliore per specificare il percorso di destinazione per una directory consiste nel creare la tabella di directory nel pacchetto di installazione per fornire la posizione corretta. Per ulteriori informazioni, vedere Utilizzo della tabella directory.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Modifica del percorso di destinazione per una directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818c4e9d555244dd1637e19eb249478f13ea2d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227199"
---
# <a name="changing-the-target-location-for-a-directory"></a>Modifica del percorso di destinazione per una directory

Se possibile, il modo migliore per specificare il percorso di destinazione per una directory consiste nel creare la [tabella di directory](directory-table.md) nel pacchetto di installazione per fornire la posizione corretta. Per ulteriori informazioni, vedere [utilizzo della tabella directory](using-the-directory-table.md).

Se è necessario modificare il percorso della directory al momento dell'installazione, sono disponibili le opzioni seguenti:

-   Specificare il percorso di una directory impostando il valore di una [proprietà pubblica](public-properties.md) nella riga di comando. Durante l' [azione CostFinalize secondo](costfinalize-action.md), i percorsi di directory interni utilizzati dal programma di installazione vengono aggiornati al valore delle proprietà elencate come chiavi nella [tabella directory](directory-table.md). Per ulteriori informazioni, vedere [utilizzo delle proprietà](using-properties.md) e [impostazione dei valori delle proprietà pubbliche nella riga di comando](setting-public-property-values-on-the-command-line.md).
-   Specificare il percorso di una directory usando un'azione personalizzata. Se l'azione personalizzata deve essere eseguita prima dell' [azione CostFinalize secondo](costfinalize-action.md), è possibile usare un [tipo di azione personalizzata 51](custom-action-type-51.md) per impostare il valore di una proprietà da una stringa di testo formattato. Se l'azione personalizzata viene eseguita dopo l' [azione CostFinalize secondo](costfinalize-action.md), è possibile usare un [tipo di azione personalizzata 35](custom-action-type-35.md) per impostare il valore del percorso della directory da una stringa di testo formattato. Le azioni personalizzate che modificano una [delle proprietà della cartella di sistema](property-reference.md) devono essere incluse nelle tabelle di sequenza di esecuzione (tabella [InstallExecuteSequence](installexecutesequence-table.md) o tabella [AdminExecuteSequence](adminexecutesequence-table.md)) e nelle tabelle di sequenza dell'interfaccia utente (tabella [InstallUISequence](installuisequence-table.md) e [tabella AdminUISequence](adminuisequence-table.md)) in modo che la cartella venga modificata durante le installazioni [*complete*](f-gly.md) dell'interfaccia utente e dell'interfaccia utente di [*base*](b-gly.md) .
-   Se l'installazione esegue un' [*interfaccia utente completa*](f-gly.md), è possibile usare [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) o [SetTargetPath ControlEvent](settargetpath-controlevent.md) per impostare il percorso della directory. Controllare la proprietà [**ProductState**](productstate.md) per determinare se il prodotto che contiene il componente è già installato prima di chiamare **MsiSetTargetPath** o SetTargetPath ControlEvent. Non tentare di modificare il percorso della directory di destinazione se alcuni componenti che usano tale percorso sono già installati per l'utente corrente o per un altro utente.

Per tutte le opzioni sopra riportate si applicano le restrizioni seguenti:

-   Non tentare di modificare il percorso della directory di destinazione se alcuni componenti che usano il percorso sono già installati per l'utente corrente o per un altro utente.
-   Non tentare di modificare il percorso della directory di destinazione durante un' [installazione di manutenzione](maintenance-installation.md).

 

 



