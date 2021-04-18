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
# <a name="findrelatedproducts-action"></a><span data-ttu-id="779d1-103">Azione FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="779d1-103">FindRelatedProducts Action</span></span>

<span data-ttu-id="779d1-104">L'azione FindRelatedProducts esegue ogni record della tabella di [aggiornamento](upgrade-table.md) in sequenza e confronta il codice di aggiornamento, la versione del prodotto e la lingua di ogni riga con i prodotti installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="779d1-104">The FindRelatedProducts action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to products installed on the system.</span></span> <span data-ttu-id="779d1-105">Quando FindRelatedProducts rileva una corrispondenza tra le informazioni di aggiornamento e un prodotto installato, aggiunge il codice prodotto alla proprietà specificata nella colonna ActionProperty di UpgradeTable.</span><span class="sxs-lookup"><span data-stu-id="779d1-105">When FindRelatedProducts detects a correspondence between the upgrade information and an installed product, it appends the product code to the property specified in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="779d1-106">L'azione FindRelatedProducts viene eseguita solo la prima volta che viene installato il prodotto.</span><span class="sxs-lookup"><span data-stu-id="779d1-106">The FindRelatedProducts action only runs the first time the product is installed.</span></span> <span data-ttu-id="779d1-107">L'azione FindRelatedProducts non viene eseguita in modalità manutenzione o disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="779d1-107">The FindRelatedProducts action does not run during maintenance mode or uninstallation.</span></span>

## <a name="database-tables-queried"></a><span data-ttu-id="779d1-108">Tabelle di database sottoposte a query</span><span class="sxs-lookup"><span data-stu-id="779d1-108">Database Tables Queried</span></span>

<span data-ttu-id="779d1-109">Questa azione esegue una query nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="779d1-109">This action queries the following table:</span></span>

[<span data-ttu-id="779d1-110">Aggiorna tabella</span><span class="sxs-lookup"><span data-stu-id="779d1-110">Upgrade Table</span></span>](upgrade-table.md)

## <a name="properties-used"></a><span data-ttu-id="779d1-111">Proprietà utilizzate</span><span class="sxs-lookup"><span data-stu-id="779d1-111">Properties Used</span></span>

<span data-ttu-id="779d1-112">L'azione FindRelatedProducts usa la proprietà [**UpgradeCode**](upgradecode.md) e le informazioni sulla versione e sulla lingua create nella tabella di aggiornamento per rilevare i prodotti installati interessati dall'aggiornamento in sospeso.</span><span class="sxs-lookup"><span data-stu-id="779d1-112">The FindRelatedProducts action uses the [**UpgradeCode**](upgradecode.md) property and the version and language information authored into the Upgrade table to detect installed products affected by the pending upgrade.</span></span> <span data-ttu-id="779d1-113">Accoda il codice prodotto dei prodotti rilevati alla proprietà nella colonna ActionProperty di UpgradeTable.</span><span class="sxs-lookup"><span data-stu-id="779d1-113">It appends the product code of detected products to the property in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="779d1-114">FindRelatedProducts riconosce solo i prodotti esistenti che sono stati installati usando il Windows Installer con un file con estensione msi che definisce una proprietà [**UpgradeCode**](upgradecode.md) , una proprietà [**ProductVersion**](productversion.md) e un valore per la proprietà [**ProductLanguage**](productlanguage.md) che corrisponde a una delle lingue elencate nella proprietà di [**Riepilogo del modello**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="779d1-114">FindRelatedProducts only recognizes existing products that have been installed using the Windows Installer with an .msi that defines an [**UpgradeCode**](upgradecode.md) property, a [**ProductVersion**](productversion.md) property, and a value for the [**ProductLanguage**](productlanguage.md) property that is one of the languages listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="779d1-115">Si noti che FindRelatedProducts usa il linguaggio restituito da [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span><span class="sxs-lookup"><span data-stu-id="779d1-115">Note that FindRelatedProducts uses the language returned by [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span></span> <span data-ttu-id="779d1-116">Per il corretto funzionamento di FindRelatedProducts, l'autore del pacchetto deve assicurarsi che la proprietà [**ProductLanguage**](productlanguage.md) nella [tabella delle proprietà](property-table.md) sia impostata su una lingua elencata anche nella proprietà di [**Riepilogo del modello**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="779d1-116">For FindRelatedProducts to work correctly, the package author must be sure that the [**ProductLanguage**](productlanguage.md) property in the [Property table](property-table.md) is set to a language that is also listed in the [**Template Summary**](template-summary.md) Property.</span></span> <span data-ttu-id="779d1-117">Vedere [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="779d1-117">See [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="779d1-118">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="779d1-118">Sequence Restrictions</span></span>

<span data-ttu-id="779d1-119">FindRelatedProducts deve essere creato nella [tabella InstallUISequence](installuisequence-table.md) e nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="779d1-119">FindRelatedProducts should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence](installexecutesequence-table.md) tables.</span></span> <span data-ttu-id="779d1-120">Il programma di installazione impedisce l'esecuzione dei prodotti FindRelated in InstallExecuteSequence se l'azione è già stata eseguita in InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="779d1-120">The installer prevents FindRelated Products from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span> <span data-ttu-id="779d1-121">L'azione FindRelatedProducts deve precedere l'azione [MigrateFeatureStates](migratefeaturestates-action.md) e l'azione [RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="779d1-121">The FindRelatedProducts action must come before the [MigrateFeatureStates action](migratefeaturestates-action.md) and the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="779d1-122">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="779d1-122">ActionData Messages</span></span>

<span data-ttu-id="779d1-123">FindRelatedProducts Invia un messaggio di dati di azione per ogni prodotto correlato rilevato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="779d1-123">FindRelatedProducts sends an action data message for each related product it detects on the system.</span></span>

 

 



