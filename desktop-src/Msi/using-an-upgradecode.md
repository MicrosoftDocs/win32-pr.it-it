---
description: La UpgradeCode viene utilizzata principalmente per supportare gli aggiornamenti principali, sebbene le patch di aggiornamento di dimensioni ridotte e secondarie possano utilizzare UpgradeCode per la convalida del prodotto.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Uso di un UpgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf32d40364653527b9f906e6dd42de64bb9f697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881025"
---
# <a name="using-an-upgradecode"></a>Uso di un UpgradeCode

La [**UpgradeCode**](upgradecode.md) viene utilizzata principalmente per supportare gli aggiornamenti principali, sebbene le patch di aggiornamento di dimensioni ridotte e secondarie possano utilizzare **UpgradeCode** per la convalida del prodotto. Durante gli aggiornamenti principali, le azioni [FindRelatedProducts](findrelatedproducts-action.md), [MigrateFeatureStates](migratefeaturestates-action.md)e [RemoveExistingProducts](removeexistingproducts-action.md) rilevano, migrano e rimuovono le versioni precedenti del prodotto. L'azione FindRelatedProducts Cerca i prodotti usando i criteri basati su **UpgradeCode**, [**ProductLanguage**](productlanguage.md)e [**ProductVersion**](productversion.md). Questi criteri vengono specificati nella tabella di [aggiornamento](upgrade-table.md) .

Considerati i criteri utilizzati dall'azione [FindRelatedProducts](findrelatedproducts-action.md) , [**UpgradeCode**](upgradecode.md) può essere lo stesso per lingue e versioni diverse di un singolo prodotto. Ciò è dovuto al fatto che la tabella di [aggiornamento](upgrade-table.md) consente di distinguere i prodotti in base alla versione e alle righe della lingua.

In versioni diverse dello stesso prodotto, potrebbe non essere mai necessario modificare il [**UpgradeCode**](upgradecode.md). Ogni prodotto autonomo deve avere il proprio **UpgradeCode**. Una suite di prodotti deve avere anche il proprio **UpgradeCode**. Questa operazione consentirà al gruppo di aggiornare le versioni precedenti della suite o dei prodotti autonomi usando più righe nella [tabella di aggiornamento](upgrade-table.md).

Nei due scenari seguenti viene illustrato l'uso di [**UpgradeCode**](upgradecode.md).

-   Il prodotto A e il prodotto B sono stati forniti con lo stesso [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md)e [**UpgradeCode**](upgradecode.md). Il prodotto A e il prodotto B hanno [**ProductCodes**](productcode.md)diversi. Poiché ai prodotti è stato assegnato lo stesso **UpgradeCode**, non è possibile creare la tabella di [aggiornamento](upgrade-table.md) per distinguere la versione precedente del prodotto a dalla versione precedente del prodotto B. In questo caso, non sarà possibile installare l'aggiornamento del prodotto A che ignora il prodotto B. Poiché si tratta di prodotti diversi, è necessario assegnare a ognuno un **UpgradeCode** diverso.
-   Le versioni in inglese e francese del prodotto A sono state fornite con lo stesso [**ProductVersion**](productversion.md) e [**UpgradeCode**](upgradecode.md). Entrambe le versioni in inglese e francese del prodotto A hanno [**ProductLanguages**](productlanguage.md) e [**ProductCodes**](productcode.md)diversi. Anche se le versioni in lingua inglese e francese condividono lo stesso **UpgradeCode**, è possibile creare la tabella di [aggiornamento](upgrade-table.md) in modo che venga rilevata e aggiornata solo la versione in lingua inglese precedente e la versione francese precedente venga ignorata. Le versioni in lingue diverse di un prodotto possono usare lo stesso **UpgradeCode**.

 

 



