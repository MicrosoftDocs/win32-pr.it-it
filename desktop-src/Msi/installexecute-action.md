---
description: L'azione InstallExecute esegue uno script contenente tutte le operazioni nella sequenza di azione dall'avvio dell'installazione o dall'ultima azione InstallExecute o InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Azione InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249a83f283b3abee97fbddf99d755b158678726fbb36c066791e3f87ae718f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946129"
---
# <a name="installexecute-action"></a>Azione InstallExecute

L'azione InstallExecute esegue uno script contenente tutte le operazioni nella sequenza di azioni dall'avvio dell'installazione o dall'ultima azione InstallExecute o [dall'azione InstallExecuteAgain](installexecuteagain-action.md). L'azione InstallExecute aggiorna il sistema senza terminare la transazione.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione InstallExecute viene eseguita tra [l'azione InstallInitialize](installinitialize-action.md) e [l'azione InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

[L'azione InstallExecuteAgain](installexecuteagain-action.md) esegue la stessa operazione dell'azione InstallExecute. Poiché le tabelle di sequenza hanno una sola chiave primaria, la colonna Azione, la stessa azione non può essere ripetuta in una tabella di sequenza specifica. Esistono due azioni che esecuno la stessa operazione, InstallExecute e InstallExecuteAgain, nei casi in cui la funzionalità di InstallExecute è necessaria due volte nella tabella [InstallExecuteSequence](installexecutesequence-table.md). Per altre informazioni, vedere [Uso di una tabella di sequenza.](using-a-sequence-table.md)

 

 



