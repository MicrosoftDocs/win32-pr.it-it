---
description: Se per un utente è già installata una versione più recente, è possibile creare pacchetti di aggiornamento Windows Installer per eseguire aggiornamenti principali.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedisci l'installazione di un pacchetto obsoleto in una versione più recente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310968"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a><span data-ttu-id="8f9da-103">Impedire l'installazione di un pacchetto obsoleto in una versione più recente</span><span class="sxs-lookup"><span data-stu-id="8f9da-103">Preventing an Old Package from Installing Over a Newer Version</span></span>

<span data-ttu-id="8f9da-104">Se per un utente è già installata una versione più recente, è possibile creare pacchetti di aggiornamento Windows Installer per eseguire aggiornamenti principali.</span><span class="sxs-lookup"><span data-stu-id="8f9da-104">Windows Installer upgrade packages can be authored to have major upgrades not install if a user already has a newer version installed.</span></span> <span data-ttu-id="8f9da-105">La procedura descritta in questo argomento può impedire solo i downgrade che potrebbero essere causati dall'esecuzione di un pacchetto di aggiornamento principale.</span><span class="sxs-lookup"><span data-stu-id="8f9da-105">The procedure in this topic can only prevent downgrades that might be caused by running a major upgrade package.</span></span> <span data-ttu-id="8f9da-106">Questa procedura si basa sull' [azione FindRelatedProducts](findrelatedproducts-action.md), che viene eseguita solo durante un'installazione per la prima volta e non viene eseguita in modalità di manutenzione (reinstallazione).</span><span class="sxs-lookup"><span data-stu-id="8f9da-106">This procedure relies on the [FindRelatedProducts Action](findrelatedproducts-action.md), which only runs during a first-time installation and does not run in maintenance mode (reinstallation).</span></span> <span data-ttu-id="8f9da-107">Poiché gli aggiornamenti secondari vengono eseguiti con la reinstallazione, questa procedura non può essere utilizzata per determinare se un pacchetto di aggiornamento secondario tenta di effettuare il downgrade di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8f9da-107">Because minor upgrades are performed using reinstallation, this procedure cannot be used to determine whether a minor upgrade package is attempting to downgrade an application.</span></span> <span data-ttu-id="8f9da-108">Per ulteriori informazioni, vedere [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-108">For more information, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="8f9da-109">**Per impedire l'installazione di un pacchetto obsoleto in una versione più recente**</span><span class="sxs-lookup"><span data-stu-id="8f9da-109">**To prevent an old package from installing over a newer version**</span></span>

1.  <span data-ttu-id="8f9da-110">Immettere la proprietà [**UpgradeCode**](upgradecode.md) per il gruppo di prodotti correlati che potrebbero essere idonei a ricevere questo aggiornamento nella colonna UpgradeCode della [tabella di aggiornamento](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-110">Enter the [**UpgradeCode**](upgradecode.md) Property for the group of related products that may be eligible to receive this upgrade into the UpgradeCode column of the [Upgrade Table](upgrade-table.md).</span></span>
2.  <span data-ttu-id="8f9da-111">Immettere il flag di bit **msidbUpgradeAttributesOnlyDetect** nella colonna attributi della [tabella di aggiornamento](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-111">Enter the **msidbUpgradeAttributesOnlyDetect** bit flag in the Attributes column of the [Upgrade Table](upgrade-table.md).</span></span>
3.  <span data-ttu-id="8f9da-112">Immettere la versione dell'aggiornamento fornito dal pacchetto nella colonna VersionMin della [tabella di aggiornamento](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-112">Enter the version of the upgrade provided by this package into the VersionMin column of the [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="8f9da-113">Lasciare vuota la colonna VersionMax.</span><span class="sxs-lookup"><span data-stu-id="8f9da-113">Leave the VersionMax column blank.</span></span>
4.  <span data-ttu-id="8f9da-114">Immettere il nome della proprietà che deve essere impostata dall' [azione FindRelatedProducts](findrelatedproducts-action.md) nella colonna ActionProperty della [tabella di aggiornamento](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-114">Enter the name of the property that is to be set by the [FindRelatedProducts Action](findrelatedproducts-action.md) into the ActionProperty column of the [Upgrade Table](upgrade-table.md).</span></span>
5.  <span data-ttu-id="8f9da-115">Aggiungere la proprietà [**SecureCustomProperties**](securecustomproperties.md) e la proprietà denominata nella colonna ActionProperty della tabella di [aggiornamento](upgrade-table.md) alla tabella delle [proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-115">Add the [**SecureCustomProperties**](securecustomproperties.md) property and the property named in the ActionProperty column of the [Upgrade Table](upgrade-table.md) to the [Property Table](property-table.md).</span></span>
6.  <span data-ttu-id="8f9da-116">Aggiungere un [tipo di azione personalizzata 19](custom-action-type-19.md) dopo l'azione FindRelatedProducts nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-116">Add a [Custom Action Type 19](custom-action-type-19.md) after the FindRelatedProducts action in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span> <span data-ttu-id="8f9da-117">Includere un record nella [tabella CustomAction](customaction-table.md) per questa azione e immettere il testo da visualizzare nella colonna destinazione.</span><span class="sxs-lookup"><span data-stu-id="8f9da-117">Include a record in the [CustomAction Table](customaction-table.md) for this action and enter the text to be displayed in the Target column.</span></span> <span data-ttu-id="8f9da-118">Il tipo 19 azione personalizzata è incorporato nel programma di installazione, quindi non è disponibile codice da scrivere.</span><span class="sxs-lookup"><span data-stu-id="8f9da-118">The type 19 custom action is built into the installer, so there is no code to write.</span></span>
7.  <span data-ttu-id="8f9da-119">Immettere il nome del ActionProperty nella colonna condizione del record nella [tabella InstallExecuteSequence](installexecutesequence-table.md) che contiene il [tipo di azione personalizzata 19](custom-action-type-19.md).</span><span class="sxs-lookup"><span data-stu-id="8f9da-119">Enter the name of the ActionProperty into the Condition column of the record in [InstallExecuteSequence Table](installexecutesequence-table.md) that contains the [Custom Action Type 19](custom-action-type-19.md).</span></span> <span data-ttu-id="8f9da-120">Questa condizione consente di eseguire l'azione personalizzata solo quando la [tabella di aggiornamento](upgrade-table.md) rileva che è già installata una versione più recente.</span><span class="sxs-lookup"><span data-stu-id="8f9da-120">This conditions the custom action to only be executed when the [Upgrade Table](upgrade-table.md) detects that a newer version is already installed.</span></span>

    <span data-ttu-id="8f9da-121">Ad esempio, un pacchetto di Windows Installer che aggiorna un gruppo di prodotti correlati alla versione 3,0 può includere i record seguenti nelle tabelle di [aggiornamento](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [Proprietà](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9da-121">For example, a Windows Installer package that upgrades a group of related products to version 3.0 may include the following records in its [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [Property](property-table.md) tables.</span></span> <span data-ttu-id="8f9da-122">Tutti i prodotti correlati del gruppo hanno lo stesso UpgradeCode, ma il programma di installazione non installa il pacchetto di aggiornamento se una versione successiva alla 3,0 è già installata nel computer.</span><span class="sxs-lookup"><span data-stu-id="8f9da-122">All the related products in the group have the same UpgradeCode, but the installer does not install this upgrade package if a version later than 3.0 is already installed on the computer.</span></span> <span data-ttu-id="8f9da-123">In questo caso, il programma di installazione visualizza un messaggio di errore e l'installazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8f9da-123">In this case, the Installer presents an error message and the installation fails.</span></span> <span data-ttu-id="8f9da-124">Il pacchetto di aggiornamento versione 3,0 viene installato nelle versioni 1,0 e 2,0.</span><span class="sxs-lookup"><span data-stu-id="8f9da-124">The version 3.0 upgrade package installs over versions 1.0 and 2.0.</span></span>

    [<span data-ttu-id="8f9da-125">Aggiorna tabella</span><span class="sxs-lookup"><span data-stu-id="8f9da-125">Upgrade Table</span></span>](upgrade-table.md)

    

    | <span data-ttu-id="8f9da-126">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="8f9da-126">UpgradeCode</span></span>                            | <span data-ttu-id="8f9da-127">VersionMin</span><span class="sxs-lookup"><span data-stu-id="8f9da-127">VersionMin</span></span> | <span data-ttu-id="8f9da-128">VersionMax</span><span class="sxs-lookup"><span data-stu-id="8f9da-128">VersionMax</span></span> | <span data-ttu-id="8f9da-129">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="8f9da-129">Language</span></span> | <span data-ttu-id="8f9da-130">Attributi</span><span class="sxs-lookup"><span data-stu-id="8f9da-130">Attributes</span></span>                                | <span data-ttu-id="8f9da-131">Rimuovi</span><span class="sxs-lookup"><span data-stu-id="8f9da-131">Remove</span></span> | <span data-ttu-id="8f9da-132">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="8f9da-132">ActionProperty</span></span>  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | <span data-ttu-id="8f9da-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="8f9da-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="8f9da-134">3.0</span><span class="sxs-lookup"><span data-stu-id="8f9da-134">3.0</span></span>        |            |          | <span data-ttu-id="8f9da-135">msidbUpgradeAttributesOnlyDetect</span><span class="sxs-lookup"><span data-stu-id="8f9da-135">msidbUpgradeAttributesOnlyDetect</span></span>          |        | <span data-ttu-id="8f9da-136">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="8f9da-136">NEWPRODUCTFOUND</span></span> |
    | <span data-ttu-id="8f9da-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="8f9da-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="8f9da-138">1.0</span><span class="sxs-lookup"><span data-stu-id="8f9da-138">1.0</span></span>        | <span data-ttu-id="8f9da-139">3.0</span><span class="sxs-lookup"><span data-stu-id="8f9da-139">3.0</span></span>        |          | <span data-ttu-id="8f9da-140">msidbUpgradeAttributesVersionMinInclusive</span><span class="sxs-lookup"><span data-stu-id="8f9da-140">msidbUpgradeAttributesVersionMinInclusive</span></span> |        | <span data-ttu-id="8f9da-141">UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="8f9da-141">UPGRADEFOUND</span></span>    |

    

     

    [<span data-ttu-id="8f9da-142">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="8f9da-142">CustomAction Table</span></span>](customaction-table.md)

    

    | <span data-ttu-id="8f9da-143">Azione</span><span class="sxs-lookup"><span data-stu-id="8f9da-143">Action</span></span> | <span data-ttu-id="8f9da-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f9da-144">Type</span></span> | <span data-ttu-id="8f9da-145">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="8f9da-145">Source</span></span> | <span data-ttu-id="8f9da-146">Destinazione</span><span class="sxs-lookup"><span data-stu-id="8f9da-146">Target</span></span>                                 |
    |--------|------|--------|----------------------------------------|
    | <span data-ttu-id="8f9da-147">CA1</span><span class="sxs-lookup"><span data-stu-id="8f9da-147">CA1</span></span>    | <span data-ttu-id="8f9da-148">19</span><span class="sxs-lookup"><span data-stu-id="8f9da-148">19</span></span>   |        | <span data-ttu-id="8f9da-149">È già installato un aggiornamento superiore.</span><span class="sxs-lookup"><span data-stu-id="8f9da-149">A higher upgrade is already installed.</span></span> |

    

     

    [<span data-ttu-id="8f9da-150">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="8f9da-150">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)

    

    | <span data-ttu-id="8f9da-151">Azione</span><span class="sxs-lookup"><span data-stu-id="8f9da-151">Action</span></span>              | <span data-ttu-id="8f9da-152">Condizione</span><span class="sxs-lookup"><span data-stu-id="8f9da-152">Condition</span></span>       | <span data-ttu-id="8f9da-153">Sequenza</span><span class="sxs-lookup"><span data-stu-id="8f9da-153">Sequence</span></span> |
    |---------------------|-----------------|----------|
    | <span data-ttu-id="8f9da-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="8f9da-154">FindRelatedProducts</span></span> |                 | <span data-ttu-id="8f9da-155">200</span><span class="sxs-lookup"><span data-stu-id="8f9da-155">200</span></span>      |
    | <span data-ttu-id="8f9da-156">CA1</span><span class="sxs-lookup"><span data-stu-id="8f9da-156">CA1</span></span>                 | <span data-ttu-id="8f9da-157">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="8f9da-157">NEWPRODUCTFOUND</span></span> | <span data-ttu-id="8f9da-158">201</span><span class="sxs-lookup"><span data-stu-id="8f9da-158">201</span></span>      |

    

     

    [<span data-ttu-id="8f9da-159">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8f9da-159">Property Table</span></span>](property-table.md)

    

    | <span data-ttu-id="8f9da-160">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f9da-160">Property</span></span>                                                 | <span data-ttu-id="8f9da-161">Valore</span><span class="sxs-lookup"><span data-stu-id="8f9da-161">Value</span></span>                        |
    |----------------------------------------------------------|------------------------------|
    | [<span data-ttu-id="8f9da-162">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="8f9da-162">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="8f9da-163">NEWPRODUCTFOUND; UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="8f9da-163">NEWPRODUCTFOUND;UPGRADEFOUND</span></span> |

    

     

 

 



