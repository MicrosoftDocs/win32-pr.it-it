---
description: L'azione LaunchConditions esegue una query sulla tabella LaunchCondition e valuta le singole istruzioni condizionali registrate. Se una di queste istruzioni condizionali ha esito negativo, viene visualizzato un messaggio di errore all'utente e l'installazione viene terminata.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Azione LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307254"
---
# <a name="launchconditions-action"></a>Azione LaunchConditions

L'azione LaunchConditions esegue una query sulla [tabella LaunchCondition](launchcondition-table.md) e valuta le singole istruzioni condizionali registrate. Se una di queste istruzioni condizionali ha esito negativo, viene visualizzato un messaggio di errore all'utente e l'installazione viene terminata.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione LaunchConditions è facoltativa. Questa azione è in genere la prima nella sequenza, ma l' [azione AppSearch](appsearch-action.md) può essere sequenziata prima dell'azione LaunchConditions. Se sono presenti condizioni di avvio che non si applicano a tutte le modalità di installazione, è necessario utilizzare la proprietà modalità di installazione appropriata in un'espressione condizionale nella tabella di sequenza appropriata.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

 

 



