---
description: Un aggiornamento importante è un aggiornamento completo di un prodotto che richiede una modifica della proprietà ProductCode.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Aggiornamenti principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98c6364ca0a6d9622eaacdea6cd37a2cc2dd10b057405a99577acab5102f8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629157"
---
# <a name="major-upgrades"></a>Aggiornamenti principali

Un aggiornamento importante è un aggiornamento completo di un prodotto che richiede una modifica della [**proprietà ProductCode.**](productcode.md)

Un aggiornamento principale tipico rimuove una versione precedente di un'applicazione e installa una nuova versione. Un aggiornamento importante può riorganizzare l'albero dei componenti della funzionalità. Per altre informazioni, vedere [**ProductCode**](productcode.md) e [Modifica del codice prodotto.](changing-the-product-code.md)

Durante un aggiornamento principale tramite il programma di installazione di Windows, il programma di installazione cerca nel computer dell'utente le applicazioni correlate all'aggiornamento in sospeso e, quando ne rileva uno, recupera la versione dell'applicazione installata dal Registro di sistema. Il programma di installazione usa quindi le informazioni nel database di aggiornamento per determinare se aggiornare l'applicazione installata.

Per abilitare le funzionalità di aggiornamento del programma di installazione, ogni pacchetto deve avere una [**proprietà UpgradeCode**](upgradecode.md) e [una tabella di aggiornamento](upgrade-table.md). Ogni prodotto autonomo o suite di prodotti deve avere il proprio **UpgradeCode**. Per altre informazioni sull'uso di **UpgradeCode,** vedere la [sezione Uso di UpgradeCode.](using-an-upgradecode.md) Ogni record nella tabella Upgrade fornisce una combinazione del codice di aggiornamento, della versione del prodotto e delle informazioni sulla lingua usate per identificare un set di prodotti interessati dall'aggiornamento. Quando [l'azione FindRelatedProducts](findrelatedproducts-action.md) rileva che un prodotto interessato è installato nel sistema, aggiunge il codice prodotto a una proprietà nella colonna ActionProperty della tabella Upgrade. [L'azione RemoveExistingProducts](removeexistingproducts-action.md) e [l'azione MigrateFeatureStates](migratefeaturestates-action.md) rimuovono o e migrano i prodotti elencati nell'elenco ActionProperty. Gli autori di pacchetti possono anche seguire la procedura descritta nell'argomento Preparazione [di un'applicazione per gli aggiornamenti principali futuri.](preparing-an-application-for-future-major-upgrades.md)

Windows I pacchetti di aggiornamento del programma di installazione possono essere creati in modo che gli aggiornamenti principali non verranno installati se l'utente dispone già di una versione più recente dell'applicazione installata. Per altre informazioni su come creare un pacchetto che non verrà installato in una versione più [recente,](preventing-an-old-package-from-installing-over-a-newer-version.md) vedere Impedire l'installazione di un pacchetto precedente in una versione più recente

> [!Note]  
> Windows Il programma di installazione usa solo i primi tre campi della versione del prodotto. Per le descrizioni di questi campi, vedere Proprietà [**ProductVersion.**](productversion.md) Se si include un quarto campo nella versione del prodotto, il programma di installazione ignora il quarto campo.

 

Metodo consigliato per applicare un aggiornamento principale installando il pacchetto completo per il prodotto aggiornato. Per informazioni su come applicare un aggiornamento principale installando il prodotto, vedere [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).

Un aggiornamento principale applicato come [patch per](patch-packages.md) il prodotto non può essere sequenziato con altri aggiornamenti e non è una [patch disinstallabile.](uninstallable-patches.md) Per informazioni su come applicare un pacchetto di patch di aggiornamento principale a un pacchetto del programma di installazione di Windows, vedere [Applying Major Upgrades by Patching the Local Installation of the Product](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). L'applicazione di un aggiornamento principale tramite un pacchetto di patch non è consigliata, ma applica gli aggiornamenti principali installando il prodotto completo.

> [!Note]  
> Se un'applicazione viene installata nel contesto di installazione per [utente,](installation-context.md)qualsiasi aggiornamento principale all'applicazione deve essere eseguito anche usando il contesto per utente. Se un'applicazione viene installata nel contesto di installazione per computer, è necessario eseguire anche qualsiasi aggiornamento principale all'applicazione usando il contesto per computer. Il Windows non installerà gli aggiornamenti principali nel contesto di installazione.

 

È possibile condizionare le azioni personalizzate sequenziate dopo [InstallValidate](installvalidate-action.md) per gestire gli aggiornamenti principali usando la [**proprietà UPGRADINGPRODUCTCODE:**](upgradingproductcode.md)

-   Se si vuole eseguire un'azione personalizzata durante una disinstallazione del prodotto, ma non durante la rimozione del prodotto da un aggiornamento principale, usare questa condizione.

    REMOVE="ALL" E NON [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Se si vuole che un'azione personalizzata sia eseguita solo durante un aggiornamento principale, usare questa condizione.

    [**AGGIORNAMENTO DIPRODUCTCODE**](upgradingproductcode.md)

 

 



