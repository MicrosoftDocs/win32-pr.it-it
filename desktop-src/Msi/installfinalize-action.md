---
description: L'azione InstallFinalize esegue uno script che contiene tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'esecuzione delle azioni InstallExecute o InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Azione InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96296c2241f5769296b7192ce89ab9f44364bb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753519"
---
# <a name="installfinalize-action"></a>Azione InstallFinalize

L'azione InstallFinalize esegue uno script che contiene tutte le operazioni nella sequenza di azione a partire dall'inizio dell'installazione o dall'esecuzione delle azioni [InstallExecute](installexecute-action.md) o [InstallExecuteAgain](installexecuteagain-action.md) . Questa azione contrassegna la fine di una transazione che inizia con l'azione [InstallInitialize](installinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [InstallInitialize](installinitialize-action.md) deve precedere l'azione InstallFinalize.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Se viene rilevato che il prodotto è contrassegnato per la rimozione completa, le operazioni vengono aggiunte automaticamente allo script per rimuovere l' **Installazione applicazioni** nelle informazioni sul **Pannello di controllo** del prodotto, per annullare la registrazione e annullare la pubblicazione del prodotto e per rimuovere il database locale memorizzato nella cache da% Windows%, se esistente.

Le modifiche di sistema apportate prima dell'azione potrebbero non essere ripristinate dopo l'esecuzione dell'azione InstallFinalize. L'azione InstallFinalize aggiorna il sistema con tutte le operazioni determinate a tale punto e quindi termina la transazione.

 

 



