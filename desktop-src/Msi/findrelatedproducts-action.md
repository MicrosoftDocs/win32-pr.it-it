---
description: L'azione FindRelatedProducts esegue ogni record della tabella di aggiornamento in sequenza e confronta il codice di aggiornamento, la versione del prodotto e la lingua di ogni riga con i prodotti installati nel sistema.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Azione FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347166"
---
# <a name="findrelatedproducts-action"></a>Azione FindRelatedProducts

L'azione FindRelatedProducts esegue ogni record della tabella di [aggiornamento](upgrade-table.md) in sequenza e confronta il codice di aggiornamento, la versione del prodotto e la lingua di ogni riga con i prodotti installati nel sistema. Quando FindRelatedProducts rileva una corrispondenza tra le informazioni di aggiornamento e un prodotto installato, aggiunge il codice prodotto alla proprietà specificata nella colonna ActionProperty di UpgradeTable.

L'azione FindRelatedProducts viene eseguita solo la prima volta che viene installato il prodotto. L'azione FindRelatedProducts non viene eseguita in modalità manutenzione o disinstallazione.

## <a name="database-tables-queried"></a>Tabelle di database sottoposte a query

Questa azione esegue una query nella tabella seguente:

[Aggiorna tabella](upgrade-table.md)

## <a name="properties-used"></a>Proprietà utilizzate

L'azione FindRelatedProducts usa la proprietà [**UpgradeCode**](upgradecode.md) e le informazioni sulla versione e sulla lingua create nella tabella di aggiornamento per rilevare i prodotti installati interessati dall'aggiornamento in sospeso. Accoda il codice prodotto dei prodotti rilevati alla proprietà nella colonna ActionProperty di UpgradeTable.

FindRelatedProducts riconosce solo i prodotti esistenti che sono stati installati usando il Windows Installer con un file con estensione msi che definisce una proprietà [**UpgradeCode**](upgradecode.md) , una proprietà [**ProductVersion**](productversion.md) e un valore per la proprietà [**ProductLanguage**](productlanguage.md) che corrisponde a una delle lingue elencate nella proprietà di [**Riepilogo del modello**](template-summary.md) .

Si noti che FindRelatedProducts usa il linguaggio restituito da [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Per il corretto funzionamento di FindRelatedProducts, l'autore del pacchetto deve assicurarsi che la proprietà [**ProductLanguage**](productlanguage.md) nella [tabella delle proprietà](property-table.md) sia impostata su una lingua elencata anche nella proprietà di [**Riepilogo del modello**](template-summary.md) . Vedere [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

FindRelatedProducts deve essere creato nella [tabella InstallUISequence](installuisequence-table.md) e nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md) . Il programma di installazione impedisce l'esecuzione dei prodotti FindRelated in InstallExecuteSequence se l'azione è già stata eseguita in InstallUISequence. L'azione FindRelatedProducts deve precedere l'azione [MigrateFeatureStates](migratefeaturestates-action.md) e l'azione [RemoveExistingProducts](removeexistingproducts-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

FindRelatedProducts Invia un messaggio di dati di azione per ogni prodotto correlato rilevato nel sistema.

 

 



