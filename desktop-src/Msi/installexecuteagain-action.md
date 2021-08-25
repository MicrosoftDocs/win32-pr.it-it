---
description: L'azione InstallExecuteAgain esegue uno script contenente tutte le operazioni nella sequenza di azioni dall'avvio dell'installazione o dall'ultima azione InstallExecuteAgain o dall'ultima azione InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Azione InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2133fcf7acee7027337864eb8e33b6b297499e96979155f066538edbd6fec00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893981"
---
# <a name="installexecuteagain-action"></a>Azione InstallExecuteAgain

L'azione InstallExecuteAgain esegue uno script contenente tutte le operazioni nella sequenza di azioni dall'avvio dell'installazione o dall'ultima azione InstallExecuteAgain o dall'ultima [azione InstallExecute](installexecute-action.md). L'azione InstallExecute aggiorna il sistema senza terminare la transazione. InstallExecuteAgain esegue la stessa operazione [dell'azione InstallExecute,](installexecute-action.md) ma deve essere usata solo dopo InstallExecute.

InstallExecuteAgain deve sempre essere impostato in modo che non sia eseguito durante la rimozione. Per informazioni, vedere [Uso delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione InstallExecute viene eseguita tra [l'azione InstallInitialize](installinitialize-action.md) e [l'azione InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

L'azione InstallExecuteAgain esegue la stessa operazione [dell'azione InstallExecute](installexecute-action.md). Poiché le tabelle di sequenza hanno una sola chiave primaria, la colonna Azione, la stessa azione non può essere ripetuta in una tabella di sequenza specifica. Esistono due azioni che eseguino la stessa operazione, InstallExecute e InstallExecuteAgain, per i casi in cui la funzionalità di InstallExecute è necessaria due volte nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Per altre informazioni, vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

 

 



