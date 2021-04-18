---
description: Un aggiornamento principale è un aggiornamento completo di un prodotto che richiede una modifica della proprietà ProductCode.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Aggiornamenti principali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7795695072f6c153373db914781ac4b919cd2572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527031"
---
# <a name="major-upgrades"></a>Aggiornamenti principali

Un aggiornamento principale è un aggiornamento completo di un prodotto che richiede una modifica della proprietà [**ProductCode**](productcode.md) .

Un tipico aggiornamento principale rimuove una versione precedente di un'applicazione e installa una nuova versione. Un aggiornamento principale può riorganizzare l'albero dei componenti della funzionalità. Per ulteriori informazioni, vedere [**ProductCode**](productcode.md) e [modifica del codice del prodotto](changing-the-product-code.md).

Durante un aggiornamento principale con Windows Installer, il programma di installazione Cerca nel computer dell'utente le applicazioni correlate all'aggiornamento in sospeso e, quando ne rileva uno, recupera la versione dell'applicazione installata dal registro di sistema. Il programma di installazione usa quindi le informazioni nel database di aggiornamento per determinare se aggiornare l'applicazione installata.

Per abilitare le funzionalità di aggiornamento del programma di installazione, ogni pacchetto deve disporre di una proprietà [**UpgradeCode**](upgradecode.md) e di una [tabella di aggiornamento](upgrade-table.md). Ogni prodotto autonomo o gruppo di prodotti deve avere il proprio **UpgradeCode**. Per altre informazioni sull'uso di **UpgradeCode** , vedere la sezione [uso di un UpgradeCode](using-an-upgradecode.md). Ogni record nella tabella di aggiornamento fornisce una combinazione del codice di aggiornamento, della versione del prodotto e delle informazioni sulla lingua utilizzate per identificare un set di prodotti interessati dall'aggiornamento. Quando l' [azione FindRelatedProducts](findrelatedproducts-action.md) rileva che nel sistema è installato un prodotto interessato, questo Accoda il codice prodotto a una proprietà nella colonna ActionProperty della tabella di aggiornamento. L' [azione RemoveExistingProducts](removeexistingproducts-action.md) e l' [azione MigrateFeatureStates](migratefeaturestates-action.md) rimuovere o migrare i prodotti elencati nell'elenco ActionProperty. Gli autori di pacchetti possono inoltre attenersi alla procedura descritta nell'argomento [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).

È possibile creare Windows Installer pacchetti di aggiornamento in modo che gli aggiornamenti principali non vengano installati se per l'utente è già installata una versione più recente dell'applicazione. Per ulteriori informazioni su come creare un pacchetto che non viene installato in una versione più recente, vedere [impedire l'installazione di un pacchetto obsoleto in una versione più recente](preventing-an-old-package-from-installing-over-a-newer-version.md) .

> [!Note]  
> Windows Installer utilizza solo i primi tre campi della versione del prodotto. Per le descrizioni di questi campi, vedere proprietà [**ProductVersion**](productversion.md) . Se si include un quarto campo nella versione del prodotto, il programma di installazione ignorerà il quarto campo.

 

Il metodo consigliato per applicare un aggiornamento principale installando il pacchetto completo per il prodotto aggiornato. Per informazioni su come applicare un aggiornamento importante installando il prodotto, vedere l'articolo relativo all' [applicazione degli aggiornamenti principali tramite l'installazione del prodotto](applying-major-upgrades-by-installing-the-product.md).

Un aggiornamento principale applicato come [pacchetto di patch](patch-packages.md) per il prodotto non può essere sequenziato con altri aggiornamenti e non è una [patch non installabile](uninstallable-patches.md). Per informazioni su come applicare un pacchetto di patch di aggiornamento principale a un pacchetto di Windows Installer, vedere [l'articolo relativo all'applicazione di aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). L'applicazione di un aggiornamento principale usando un pacchetto di patch non è consigliata, ma è consigliabile applicare gli aggiornamenti principali installando il prodotto completo.

> [!Note]  
> Se un'applicazione viene installata nel [contesto di installazione](installation-context.md)per utente, è necessario eseguire qualsiasi aggiornamento importante dell'applicazione anche usando il contesto per utente. Se un'applicazione viene installata nel contesto di installazione per computer, è necessario eseguire anche eventuali aggiornamenti principali dell'applicazione usando il contesto per computer. Il Windows Installer non installerà gli aggiornamenti principali nel contesto di installazione.

 

È possibile condizionare le azioni personalizzate sequenziate dopo [InstallValidate](installvalidate-action.md) per gestire gli aggiornamenti principali usando la proprietà [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) :

-   Se si desidera che un'azione personalizzata venga eseguita durante una disinstallazione del prodotto, ma non durante la rimozione del prodotto da un aggiornamento principale, utilizzare questa condizione.

    REMOVE = "ALL" e non [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Se si vuole che un'azione personalizzata venga eseguita solo durante un aggiornamento principale, usare questa condizione.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 



