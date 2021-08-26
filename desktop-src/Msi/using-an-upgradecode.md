---
description: UpgradeCode viene usato principalmente per supportare gli aggiornamenti principali, anche se le patch di aggiornamento di piccole e piccole dimensioni possono usare UpgradeCode per la convalida del prodotto.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Uso di UpgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482bdaa228bc57432ab730e59f265fc50352c3a63ed29f75ee0a63c65c201ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039091"
---
# <a name="using-an-upgradecode"></a>Uso di UpgradeCode

[**UpgradeCode viene usato**](upgradecode.md) principalmente per supportare gli aggiornamenti principali, anche se le patch di aggiornamento di piccole e piccole dimensioni possono usare **UpgradeCode** per la convalida del prodotto. Durante gli aggiornamenti principali, le azioni [FindRelatedProducts,](findrelatedproducts-action.md) [MigrateFeatureStates](migratefeaturestates-action.md)e [RemoveExistingProducts](removeexistingproducts-action.md) rilevano, migrano e rimuovono le versioni precedenti del prodotto. L'azione FindRelatedProducts cerca i prodotti usando criteri basati su **UpgradeCode**, [**ProductLanguage**](productlanguage.md)e [**ProductVersion**](productversion.md). Questi criteri vengono specificati nella [tabella Upgrade.](upgrade-table.md)

Dati i criteri usati [dall'azione FindRelatedProducts,](findrelatedproducts-action.md) [**UpgradeCode**](upgradecode.md) può essere lo stesso per lingue e versioni diverse di un singolo prodotto. Ciò è dovuto al [fatto che la](upgrade-table.md) tabella Upgrade consente di differenziare i prodotti in base alla versione e alla lingua.

In versioni diverse dello stesso prodotto, potrebbe non essere mai necessario modificare [**upgradeCode.**](upgradecode.md) Ogni prodotto autonomo deve avere il proprio **UpgradeCode**. Una suite di prodotti deve avere anche il proprio **UpgradeCode**. In questo modo il gruppo di prodotti sarà in grado di aggiornare le versioni precedenti della suite o dei prodotti autonomi usando più righe nella [tabella Di aggiornamento](upgrade-table.md).

I due scenari seguenti illustrano l'uso di [**UpgradeCode**](upgradecode.md).

-   Il prodotto A e il prodotto B sono stati spediti con gli stessi [**codici ProductLanguage,**](productlanguage.md) [**ProductVersion**](productversion.md) [**e UpgradeCode.**](upgradecode.md) Il prodotto A e il prodotto B hanno [**Codici Prodotto diversi.**](productcode.md) Poiché ai prodotti è stato assegnato lo stesso **UpgradeCode**, non è possibile creare la tabella [Upgrade](upgrade-table.md) per distinguere la versione precedente del Prodotto A dalla versione precedente del Prodotto B. In questo caso, non sarà possibile avere un'installazione di aggiornamento del prodotto A che ignora il prodotto B. Poiché si tratta di prodotti diversi, a ognuno di essi dovrebbe essere stato assegnato **un valore UpgradeCode diverso.**
-   Le versioni in inglese e francese del prodotto A sono state fornite con gli stessi [**productversion**](productversion.md) e [**upgradecode**](upgradecode.md). Sia le versioni in inglese che in francese del prodotto A hanno [**codici ProductLanguage e**](productlanguage.md) [**ProductLanguage diversi.**](productcode.md) Anche se entrambe le versioni in lingua inglese e francese condividono lo stesso **codice** di aggiornamento, è possibile creare la tabella [Di](upgrade-table.md) aggiornamento in modo che solo la versione in lingua inglese precedente verrà rilevata e aggiornata e la versione francese precedente verrà ignorata. Versioni in lingue diverse di un prodotto possono usare lo stesso **upgradecode.**

 

 



