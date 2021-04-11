---
description: L'azione InstallExecute esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecute o InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Azione InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128379"
---
# <a name="installexecute-action"></a>Azione InstallExecute

L'azione InstallExecute esegue uno script contenente tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'ultima azione InstallExecute o [InstallExecuteAgain](installexecuteagain-action.md). L'azione InstallExecute aggiorna il sistema senza terminare la transazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione InstallExecute viene eseguita tra l' [azione InstallInitialize](installinitialize-action.md) e l' [azione InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

L' [azione InstallExecuteAgain](installexecuteagain-action.md) esegue la stessa operazione dell'azione InstallExecute. Poiché le tabelle di sequenza includono solo una chiave primaria, la colonna azione non può essere ripetuta in una determinata tabella di sequenza. Esistono due azioni che eseguono la stessa operazione, InstallExecute e InstallExecuteAgain, per i casi in cui la funzionalità di InstallExecute è necessaria due volte nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

 

 



