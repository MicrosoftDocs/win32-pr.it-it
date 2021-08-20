---
description: L'azione FindRelatedProducts viene eseguita in ogni record della tabella Upgrade in sequenza e confronta il codice di aggiornamento, la versione del prodotto e la lingua in ogni riga con i prodotti installati nel sistema.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Azione FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8201a2e86f9dec09931b17cd4dd594c45e4bf78de32ba438b8824a6f540563fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142880"
---
# <a name="findrelatedproducts-action"></a>Azione FindRelatedProducts

L'azione FindRelatedProducts viene eseguita in ogni record della tabella [Upgrade](upgrade-table.md) in sequenza e confronta il codice di aggiornamento, la versione del prodotto e la lingua in ogni riga con i prodotti installati nel sistema. Quando FindRelatedProducts rileva una corrispondenza tra le informazioni di aggiornamento e un prodotto installato, aggiunge il codice prodotto alla proprietà specificata nella colonna ActionProperty di UpgradeTable.

L'azione FindRelatedProducts viene eseguita solo alla prima installazione del prodotto. L'azione FindRelatedProducts non viene eseguita durante la modalità di manutenzione o la disinstallazione.

## <a name="database-tables-queried"></a>Tabelle di database su cui è stata eseguita una query

Questa azione esegue una query nella tabella seguente:

[Aggiornare la tabella](upgrade-table.md)

## <a name="properties-used"></a>Proprietà usate

L'azione FindRelatedProducts usa la [**proprietà UpgradeCode**](upgradecode.md) e le informazioni sulla versione e sulla lingua scritte nella tabella Upgrade per rilevare i prodotti installati interessati dall'aggiornamento in sospeso. Aggiunge il codice prodotto dei prodotti rilevati alla proprietà nella colonna ActionProperty di UpgradeTable.

FindRelatedProducts riconosce solo i prodotti esistenti installati usando il programma di installazione di Windows con un .msi che definisce una [**proprietà UpgradeCode,**](upgradecode.md) una proprietà [**ProductVersion**](productversion.md) e un valore per la [**proprietà ProductLanguage**](productlanguage.md) che è una delle lingue elencate nella proprietà [**Riepilogo**](template-summary.md) modello.

Si noti che FindRelatedProducts usa la lingua restituita da [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Per il corretto funzionamento di FindRelatedProducts, l'autore del pacchetto deve assicurarsi che la proprietà [**ProductLanguage**](productlanguage.md) nella tabella [Proprietà](property-table.md) sia impostata su una lingua elencata anche nella proprietà [**Riepilogo**](template-summary.md) modello. Vedere [Preparazione di un'applicazione per gli aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

FindRelatedProducts deve essere creato nella [tabella InstallUISequence](installuisequence-table.md) e [nelle tabelle InstallExecuteSequence.](installexecutesequence-table.md) Il programma di installazione impedisce l'esecuzione di FindRelated Products in InstallExecuteSequence se l'azione è già stata eseguita in InstallUISequence. L'azione FindRelatedProducts deve essere eseguita prima [dell'azione MigrateFeatureStates](migratefeaturestates-action.md) e [dell'azione RemoveExistingProducts](removeexistingproducts-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

FindRelatedProducts invia un messaggio di dati azione per ogni prodotto correlato rilevato nel sistema.

 

 



