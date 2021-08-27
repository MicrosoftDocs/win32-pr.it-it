---
description: L'azione LaunchConditions esegue una query sulla tabella LaunchCondition e valuta ogni istruzione condizionale registrata in questa tabella. Se una di queste istruzioni condizionali ha esito negativo, viene visualizzato un messaggio di errore per l'utente e l'installazione viene terminata.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Azione LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a973e6e1de81091039de12e07e8edb890c860e5be54e942f00406e39e62e229
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086031"
---
# <a name="launchconditions-action"></a>Azione LaunchConditions

L'azione LaunchConditions esegue una query [sulla tabella LaunchCondition](launchcondition-table.md) e valuta ogni istruzione condizionale registrata in questa tabella. Se una di queste istruzioni condizionali ha esito negativo, viene visualizzato un messaggio di errore per l'utente e l'installazione viene terminata.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione LaunchConditions è facoltativa. Questa azione è in genere la prima nella sequenza, ma [l'azione AppSearch](appsearch-action.md) può essere sequenziata prima dell'azione LaunchConditions. Se sono presenti condizioni di avvio che non si applicano a tutte le modalità di installazione, è necessario usare la proprietà modalità di installazione appropriata in un'espressione condizionale nella tabella di sequenza appropriata.

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

 

 



