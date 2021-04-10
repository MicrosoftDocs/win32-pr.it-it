---
description: L'azione InstallExecuteAgain esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecuteAgain o dall'ultima azione InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Azione InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966604"
---
# <a name="installexecuteagain-action"></a>Azione InstallExecuteAgain

L'azione InstallExecuteAgain esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecuteAgain o dall'ultima [azione InstallExecute](installexecute-action.md). L'azione InstallExecute aggiorna il sistema senza terminare la transazione. InstallExecuteAgain esegue la stessa operazione dell' [azione InstallExecute](installexecute-action.md) , ma deve essere utilizzata solo dopo InstallExecute.

InstallExecuteAgain deve sempre essere impostato in modo che non venga eseguito durante la rimozione. Per informazioni, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione InstallExecute viene eseguita tra l' [azione InstallInitialize](installinitialize-action.md) e l' [azione InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L'azione InstallExecuteAgain esegue la stessa operazione dell' [azione InstallExecute](installexecute-action.md). Poiché le tabelle di sequenza includono solo una chiave primaria, la colonna azione non può essere ripetuta in una determinata tabella di sequenza. Esistono due azioni che eseguono la stessa operazione, InstallExecute e InstallExecuteAgain, per i casi in cui la funzionalità di InstallExecute è necessaria due volte nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

 

 



