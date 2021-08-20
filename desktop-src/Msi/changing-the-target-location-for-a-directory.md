---
description: Se possibile, il modo migliore per specificare il percorso di destinazione per una directory è creare la tabella di directory nel pacchetto di installazione per fornire il percorso corretto. Per altre informazioni, vedere Uso della tabella directory.
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: Modifica del percorso di destinazione per una directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27adf952faeb4d37d5edb08a04bf25cc640d41e5d87732b30c80d25bba729705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145684"
---
# <a name="changing-the-target-location-for-a-directory"></a>Modifica del percorso di destinazione per una directory

Se possibile, il modo migliore per specificare il percorso di destinazione per una directory è creare la [tabella di directory](directory-table.md) nel pacchetto di installazione per fornire il percorso corretto. Per altre informazioni, vedere [Uso della tabella directory](using-the-directory-table.md).

Se è necessario modificare il percorso della directory al momento dell'installazione, sono disponibili le opzioni seguenti:

-   Specificare il percorso di una directory impostando il valore di [una proprietà pubblica](public-properties.md) nella riga di comando. Durante [l'azione CostFinalize](costfinalize-action.md), i percorsi di directory interni usati dal programma di installazione vengono aggiornati al valore delle proprietà elencate come chiavi nella [tabella directory](directory-table.md). Per altre informazioni, vedere [Uso delle proprietà e](using-properties.md) Impostazione di valori di proprietà pubbliche nella riga di [comando](setting-public-property-values-on-the-command-line.md).
-   Specificare il percorso di una directory usando un'azione personalizzata. Se l'azione personalizzata deve essere eseguita prima dell'azione [CostFinalize](costfinalize-action.md), è possibile usare un tipo di azione personalizzata [51](custom-action-type-51.md) per impostare il valore di una proprietà da una stringa di testo formattata. Se l'azione personalizzata viene eseguita dopo [l'azione CostFinalize](costfinalize-action.md), è possibile usare un tipo di azione personalizzata [35](custom-action-type-35.md) per impostare il valore del percorso della directory da una stringa di testo formattata. Le azioni personalizzate che [](property-reference.md) modificano una delle proprietà della cartella di sistema devono essere incluse sia nelle tabelle della sequenza di esecuzione ( Tabella[InstallExecuteSequence](installexecutesequence-table.md) [](b-gly.md) o [AdminExecuteSequence Table](adminexecutesequence-table.md) [](f-gly.md) ) che nelle tabelle della sequenza dell'interfaccia utente ([Tabella InstallUISequence](installuisequence-table.md) e [Tabella AdminUISequence](adminuisequence-table.md)) in modo che la cartella sia modificata durante le installazioni complete dell'interfaccia utente e di base dell'interfaccia utente.
-   Se l'installazione esegue [*un'interfaccia*](f-gly.md)utente completa, è possibile usare [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) o [SetTargetPath ControlEvent](settargetpath-controlevent.md) per impostare il percorso della directory. Controllare la [**proprietà ProductState**](productstate.md) per determinare se il prodotto che contiene questo componente è già installato prima di chiamare **MsiSetTargetPath** o SetTargetPath ControlEvent. Non tentare di modificare il percorso della directory di destinazione se alcuni componenti che usano tale percorso sono già installati per l'utente corrente o un utente diverso.

Le restrizioni seguenti si applicano a tutte le opzioni precedenti:

-   Non tentare di modificare il percorso della directory di destinazione se alcuni componenti che usano il percorso sono già installati per l'utente corrente o per un utente diverso.
-   Non tentare di modificare il percorso della directory di destinazione durante [un'installazione di manutenzione](maintenance-installation.md).

 

 



