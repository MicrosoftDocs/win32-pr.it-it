---
description: L'azione RemoveExistingProducts passa attraverso i codici prodotto elencati nella colonna ActionProperty della tabella Upgrade e rimuove i prodotti in sequenza richiamando installazioni simultanee.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Azione RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3118ebd01aa39b0d9a5dad29ad1c3563c869ed5e0ebc8dfefd5ecd5c89301f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810931"
---
# <a name="removeexistingproducts-action"></a>Azione RemoveExistingProducts

L'azione RemoveExistingProducts passa attraverso i codici prodotto elencati nella colonna ActionProperty della tabella [Upgrade](upgrade-table.md) e rimuove i prodotti in sequenza richiamando installazioni simultanee. Per ogni installazione simultanea, il programma di installazione imposta la proprietà [**ProductCode**](productcode.md) sul codice del prodotto e la [**proprietà REMOVE**](remove.md) sul valore nel campo Remove della tabella Upgrade. Se il campo Remove è vuoto, il valore predefinito è ALL e il programma di installazione rimuove l'intero prodotto.

Il programma di installazione esegue l'azione RemoveExistingProducts solo la prima volta che installa un prodotto. Non esegue l'azione durante un'installazione [o una disinstallazione](maintenance-installation.md) di manutenzione.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione RemoveExistingProducts deve essere pianificata nella sequenza di azioni in una delle posizioni seguenti.

-   Tra [l'azione InstallValidate e](installvalidate-action.md) [l'azione InstallInitialize](installinitialize-action.md). In questo caso, il programma di installazione rimuove completamente le applicazioni precedenti prima di installare le nuove applicazioni. Si tratta di una posizione inefficiente per l'azione perché è necessario ricopiare tutti i file riutilizzati.
-   Dopo [l'azione InstallInitialize e](installinitialize-action.md) prima di qualsiasi azione che genera lo script di esecuzione.
-   Tra [l'azione InstallExecute](installexecute-action.md)o [l'azione InstallExecuteAgain](installexecuteagain-action.md)e [l'azione InstallFinalize](installfinalize-action.md). In genere le ultime tre azioni vengono pianificate subito dopo l'altra: InstallExecute, RemoveExistingProducts e InstallFinalize. In questo caso i file aggiornati vengono installati per primi e quindi vengono rimossi i file vecchi. Tuttavia, se la rimozione dell'applicazione precedente non riesce, il programma di installazione esegue il rollback sia della rimozione dell'applicazione precedente che dell'installazione della nuova applicazione.
-   Dopo [l'azione InstallFinalize](installfinalize-action.md). Si tratta del posizionamento più efficiente per l'azione. In questo caso, il programma di installazione aggiorna i file prima di rimuovere le applicazioni precedenti. Durante l'installazione vengono installati solo i file aggiornati. Se la rimozione dell'applicazione precedente non riesce, il programma di installazione esegue solo il rollback della disinstallazione dell'applicazione precedente.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Prodotto rimosso.           |



 

## <a name="remarks"></a>Commenti

Windows Il programma di installazione [**imposta la proprietà UPGRADINGPRODUCTCODE**](upgradingproductcode.md) quando esegue questa azione.

 

 



