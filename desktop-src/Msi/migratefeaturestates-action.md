---
description: L'azione MigrateFeatureStates viene usata durante l'aggiornamento e durante l'installazione di una nuova applicazione in un'applicazione correlata.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Azione MigrateFeatureStates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac96a3b2babf5f92ae8078ecc703875c09a0e2f61155fd565985919b5a6393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745171"
---
# <a name="migratefeaturestates-action"></a>Azione MigrateFeatureStates

L'azione MigrateFeatureStates viene usata durante l'aggiornamento e durante l'installazione di una nuova applicazione in un'applicazione correlata. MigrateFeatureStates legge gli stati delle funzionalità nell'applicazione esistente e quindi imposta questi stati di funzionalità nell'installazione in sospeso. Il metodo è utile solo quando la nuova struttura ad albero delle funzionalità non è cambiata notevolmente rispetto all'originale.

L'azione MigrateFeatureStates viene eseguita solo alla prima installazione del prodotto. L'azione MigrateFeatureStates non viene eseguita durante la modalità di manutenzione o la disinstallazione.

L'azione MigrateFeatureStates viene eseguita in ogni record della tabella [Upgrade](upgrade-table.md) in sequenza e confronta il codice di aggiornamento, la versione del prodotto e la lingua in ogni riga con tutti i prodotti installati nel sistema. Se l'azione MigrateFeatureStates rileva una corrispondenza e se il flag di bit msidbUpgradeAttributesMigrateFeatures è impostato nella colonna Attributi della tabella Upgrade, il programma di installazione esegue una query degli stati delle funzionalità esistenti per il prodotto e imposta questi stati per le stesse funzionalità nella nuova applicazione. L'azione esegue la migrazione degli stati delle funzionalità solo se [**la proprietà Preselezionata**](preselected.md) non è impostata.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione MigrateFeatureStates dovrebbe essere eseguita immediatamente dopo [l'azione CostFinalize](costfinalize-action.md). MigrateFeatureStates deve essere sequenziata sia nella tabella [InstallUISequence](installuisequence-table.md) che nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Il programma di installazione impedisce l'esecuzione di MigrateFeatureStates in InstallExecuteSequence se l'azione è già stata eseguita in InstallUISequence.

## <a name="actiondata-messages"></a>Messaggi ActionData

MigrateFeatureSettings invia un messaggio di dati di azione per ogni prodotto.

## <a name="remarks"></a>Commenti

Se più di un prodotto installato condivide una funzionalità, lo stato di installazione di tale funzionalità può variare tra i prodotti. L'azione MigrateFeatureState usa l'ordine di precedenza seguente durante la migrazione degli stati di installazione delle funzionalità: esecuzione locale, esecuzione dall'origine, annuncio e disinstallazione. Ad esempio, il prodotto installato A può avere la funzionalità Y come INSTALLSTATE LOCAL e il prodotto B installato potrebbe avere la funzionalità \_ Y come INSTALLSTATE \_ ABSENT. Se un aggiornamento installa il prodotto C ed esegue la migrazione dello stato di installazione della funzionalità Y, MigrateFeatureState imposta lo stato di installazione della funzionalità Y nel prodotto C su INSTALLSTATE \_ LOCAL.

Per altre informazioni su come usare l'azione MigrateFeatureStates per gli aggiornamenti del prodotto, vedere Preparazione di un'applicazione per [gli aggiornamenti principali futuri.](preparing-an-application-for-future-major-upgrades.md)

 

 



