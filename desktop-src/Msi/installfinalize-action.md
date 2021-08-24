---
description: L'azione InstallFinalize esegue uno script che contiene tutte le operazioni nella sequenza di azioni dall'avvio dell'installazione o dall'esecuzione delle azioni InstallExecute o InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Azione InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8bd3ac9473fab868e5f7d83e760b39ca4dd6136faec987b5a7d2a3777bdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787041"
---
# <a name="installfinalize-action"></a>Azione InstallFinalize

L'azione InstallFinalize esegue uno script che contiene tutte le operazioni nella sequenza di azioni dall'avvio dell'installazione o dall'esecuzione delle azioni [InstallExecute](installexecute-action.md) o [InstallExecuteAgain.](installexecuteagain-action.md) Questa azione contrassegna la fine di una transazione che inizia con [l'azione InstallInitialize.](installinitialize-action.md)

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

[L'azione InstallInitialize](installinitialize-action.md) deve essere eseguita prima dell'azione InstallFinalize.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

Se viene rilevato che il prodotto è contrassegnato per la rimozione  completa, le operazioni vengono aggiunte automaticamente allo script per rimuovere le informazioni di Installazione applicazioni nel **Pannello di controllo** per il prodotto, annullare la registrazione e annullare la pubblicazione del prodotto e rimuovere il database locale memorizzato nella cache da %WINDOWS%, se presente.

Le modifiche di sistema apportate prima dell'azione potrebbero non essere ripristinate dopo l'esecuzione dell'azione InstallFinalize. L'azione InstallFinalize aggiorna il sistema con tutte le operazioni determinate fino a quel punto e quindi termina la transazione.

 

 



