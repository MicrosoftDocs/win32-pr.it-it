---
description: L'azione MigrateFeatureStates viene utilizzata durante l'aggiornamento e quando si installa una nuova applicazione in un'applicazione correlata.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Azione MigrateFeatureStates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e76edb5fa13506291cc85ebcf8c8824e4ee28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315899"
---
# <a name="migratefeaturestates-action"></a>Azione MigrateFeatureStates

L'azione MigrateFeatureStates viene utilizzata durante l'aggiornamento e quando si installa una nuova applicazione in un'applicazione correlata. MigrateFeatureStates legge gli Stati delle funzionalità nell'applicazione esistente e quindi imposta gli Stati della funzionalità nell'installazione in sospeso. Il metodo è utile solo quando la nuova struttura ad albero delle funzionalità non è stata modificata in modo sostanziale rispetto all'originale.

L'azione MigrateFeatureStates viene eseguita solo la prima volta che viene installato il prodotto. L'azione MigrateFeatureStates non viene eseguita in modalità manutenzione o disinstallazione.

L'azione MigrateFeatureStates esegue ogni record della [tabella di aggiornamento](upgrade-table.md) in sequenza e confronta il codice di aggiornamento, la versione del prodotto e la lingua di ogni riga con tutti i prodotti installati nel sistema. Se l'azione MigrateFeatureStates rileva una corrispondenza e se il flag di bit msidbUpgradeAttributesMigrateFeatures è impostato nella colonna attributi della tabella di aggiornamento, il programma di installazione esegue una query sugli Stati della funzionalità esistente per il prodotto e imposta questi stati per le stesse funzionalità della nuova applicazione. L'azione esegue solo la migrazione degli Stati della funzionalità se la proprietà [**preselezionata**](preselected.md) non è impostata.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione MigrateFeatureStates dovrebbe essere immediatamente successiva all' [azione CostFinalize secondo](costfinalize-action.md). MigrateFeatureStates deve essere sequenziato sia nella tabella [InstallUISequence](installuisequence-table.md) che nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Il programma di installazione impedisce l'esecuzione di MigrateFeatureStates in InstallExecuteSequence se l'azione è già stata eseguita in InstallUISequence.

## <a name="actiondata-messages"></a>Messaggi ActionData

MigrateFeatureSettings Invia un messaggio di dati di azione per ogni prodotto.

## <a name="remarks"></a>Commenti

Se più di un prodotto installato condivide una funzionalità, lo stato di installazione di tale funzionalità può essere diverso tra i prodotti. L'azione MigrateFeatureState usa l'ordine di precedenza seguente quando si esegue la migrazione degli Stati di installazione della funzionalità: Esegui localmente, Esegui da origine, annunciata e disinstallata. Ad esempio, il prodotto installato A può avere la funzionalità Y come INSTALLSTATE \_ locale e il prodotto B installato potrebbe avere la funzionalità y come InstallState \_ assente. Se un aggiornamento installa il prodotto C ed esegue la migrazione dello stato di installazione della funzionalità Y, MigrateFeatureState imposta lo stato di installazione della funzionalità Y nel prodotto C su INSTALLSTATE \_ locale.

Per altre informazioni su come usare l'azione MigrateFeatureStates per gli aggiornamenti del prodotto, vedere [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).

 

 



