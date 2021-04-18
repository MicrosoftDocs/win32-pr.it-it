---
description: L'azione RemoveExistingProducts passa attraverso i codici prodotto elencati nella colonna ActionProperty della tabella di aggiornamento e rimuove i prodotti in sequenza richiamando le installazioni simultanee.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Azione RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312321"
---
# <a name="removeexistingproducts-action"></a>Azione RemoveExistingProducts

L'azione RemoveExistingProducts passa attraverso i codici prodotto elencati nella colonna ActionProperty della tabella di [aggiornamento](upgrade-table.md) e rimuove i prodotti in sequenza richiamando le installazioni simultanee. Per ogni installazione simultanea, il programma di installazione imposta la proprietà [**ProductCode**](productcode.md) sul codice del prodotto e imposta la proprietà [**Remove**](remove.md) sul valore nel campo Remove della tabella upgrade. Se il campo Rimuovi è vuoto, il valore predefinito è tutti e il programma di installazione rimuove l'intero prodotto.

Il programma di installazione esegue l'azione RemoveExistingProducts alla prima installazione di un prodotto. Non esegue l'azione durante un'installazione o una disinstallazione di [manutenzione](maintenance-installation.md) .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RemoveExistingProducts deve essere pianificata nella sequenza di azione in una delle posizioni seguenti.

-   Tra l' [azione InstallValidate](installvalidate-action.md) e l' [azione InstallInitialize](installinitialize-action.md). In questo caso, il programma di installazione rimuove completamente le applicazioni precedenti prima di installare le nuove applicazioni. Si tratta di una posizione non efficiente per l'azione perché tutti i file riutilizzati devono essere ricopiati.
-   Dopo l' [azione InstallInitialize](installinitialize-action.md) e prima di qualsiasi azione che genera lo script di esecuzione.
-   Tra l'azione [InstallExecute](installexecute-action.md)o l'azione [InstallExecuteAgain](installexecuteagain-action.md)e l'azione [InstallFinalize](installfinalize-action.md). In genere le ultime tre azioni sono pianificate subito dopo un'altra: InstallExecute, RemoveExistingProducts e InstallFinalize. In questo caso i file aggiornati vengono installati per primi e i file obsoleti vengono rimossi. Tuttavia, se la rimozione dell'applicazione precedente ha esito negativo, il programma di installazione esegue il rollback sia della rimozione dell'applicazione precedente sia dell'installazione della nuova applicazione.
-   Dopo l' [azione InstallFinalize](installfinalize-action.md). Si tratta del posizionamento più efficiente per l'azione. In questo caso, il programma di installazione aggiorna i file prima di rimuovere le applicazioni precedenti. Solo i file aggiornati vengono installati durante l'installazione. Se la rimozione dell'applicazione precedente ha esito negativo, il programma di installazione esegue solo il rollback della disinstallazione dell'applicazione precedente.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Prodotto rimosso.           |



 

## <a name="remarks"></a>Commenti

Windows Installer imposta la proprietà [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) durante l'esecuzione di questa azione.

 

 



