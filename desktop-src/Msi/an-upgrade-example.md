---
description: Le sezioni seguenti presentano un esempio di creazione di un pacchetto di aggiornamento per l'applicazione descritta in un esempio di installazione.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Esempio di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311061"
---
# <a name="an-upgrade-example"></a><span data-ttu-id="2e28d-103">Esempio di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-103">An Upgrade Example</span></span>

<span data-ttu-id="2e28d-104">Le sezioni seguenti presentano un esempio di creazione di un pacchetto di aggiornamento per l'applicazione descritta in [un esempio di installazione](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="2e28d-104">The following sections present an example of authoring an upgrade package for the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="2e28d-105">Un esempio di interfaccia utente minima per questo esempio è disponibile nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md) come file Uisample.msi.</span><span class="sxs-lookup"><span data-stu-id="2e28d-105">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="2e28d-106">Se si dispone dell'SDK, è possibile accedere a tutti gli strumenti e i dati necessari per riprodurre il pacchetto di installazione di esempio, l'interfaccia utente e il pacchetto di aggiornamento di esempio.</span><span class="sxs-lookup"><span data-stu-id="2e28d-106">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and sample upgrade package.</span></span>

<span data-ttu-id="2e28d-107">Questo esempio illustra come creare un pacchetto di Windows Installer che aggiorna il prodotto ipotetico MNP2000 a un nuovo prodotto denominato MNP2001.</span><span class="sxs-lookup"><span data-stu-id="2e28d-107">This example illustrates how to create a Windows Installer package that upgrades the hypothetical product MNP2000 to a new product called MNP2001.</span></span> <span data-ttu-id="2e28d-108">Il pacchetto di aggiornamento di esempio applica un aggiornamento principale al prodotto che richiede la modifica del codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="2e28d-108">The example upgrade package applies a major upgrade to the product which requires changing the product code.</span></span> <span data-ttu-id="2e28d-109">Per ulteriori informazioni sugli aggiornamenti principali, vedere l'argomento relativo agli [aggiornamenti principali](major-upgrades.md) nella sezione applicazione di [patch e aggiornamenti](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="2e28d-109">For more information about major upgrades, see the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section.</span></span>

<span data-ttu-id="2e28d-110">Il pacchetto di aggiornamento di esempio presenta le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="2e28d-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="2e28d-111">Per qualificarsi per la ricezione dell'aggiornamento a MNP2001, un utente deve avere installato in precedenza le versioni da 1,0 a 1,4 (incluse) della lingua inglese MNP2000 usando Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2e28d-111">To qualify to receive this upgrade to MNP2001, a user must have previously installed the 1.0 to 1.4 (inclusive) versions of English language MNP2000 using Windows Installer.</span></span>
-   <span data-ttu-id="2e28d-112">Quando un utente tenta di installare il pacchetto di aggiornamento, la funzionalità di aggiornamento di Windows Installer cerca nel computer dell'utente tutti i prodotti che sono idonei per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2e28d-112">When a user attempts to install the upgrade package, the upgrade functionality of Windows Installer searches the user's computer for any products that qualify for the upgrade.</span></span>
-   <span data-ttu-id="2e28d-113">Windows Installer esegue la migrazione di tutte le impostazioni della funzionalità del prodotto originale al prodotto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="2e28d-113">Windows Installer migrates all the of the original product's feature settings to the upgraded product.</span></span>
-   <span data-ttu-id="2e28d-114">Il programma di installazione rimuove tutte le funzionalità obsolete dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2e28d-114">The installer removes all obsolete features from the user's computer.</span></span>
-   <span data-ttu-id="2e28d-115">Il programma di installazione installa tutte le nuove funzionalità appartenenti all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2e28d-115">The installer installs all new features belonging to the upgrade.</span></span>
-   <span data-ttu-id="2e28d-116">Una disinstallazione del pacchetto di aggiornamento comporta la rimozione del prodotto dal computer dell'utente e non il ripristino della versione precedente del prodotto.</span><span class="sxs-lookup"><span data-stu-id="2e28d-116">An uninstall of the upgrade package removes the product from the user's computer, and does not restore the earlier version of the product.</span></span>
-   <span data-ttu-id="2e28d-117">L'aggiornamento di esempio aggiorna i collegamenti ai nuovi file e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="2e28d-117">The sample upgrade updates shortcuts to new files and features.</span></span>

    [<span data-ttu-id="2e28d-118">Pianificazione di un aggiornamento principale</span><span class="sxs-lookup"><span data-stu-id="2e28d-118">Planning a Major Upgrade</span></span>](planning-a-major-upgrade.md)

    [<span data-ttu-id="2e28d-119">Importazione del database di installazione originale</span><span class="sxs-lookup"><span data-stu-id="2e28d-119">Importing Original Installation Database</span></span>](importing-original-installation-database.md)

    [<span data-ttu-id="2e28d-120">Aggiornamento della struttura di directory per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-120">Updating Directory Structure for an Upgrade</span></span>](updating-directory-structure-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-121">Aggiornamento di file e attributi di file per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-121">Updating Files and File Attributes for an Upgrade</span></span>](updating-files-and-file-attributes-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-122">Aggiornamento dei componenti per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-122">Updating Components for an Upgrade</span></span>](updating-components-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-123">Aggiornamento delle funzionalità per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-123">Updating Features for an Upgrade</span></span>](updating-features-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-124">Aggiornamento dei collegamenti per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-124">Updating Shortcuts for an Upgrade</span></span>](updating-shortcuts-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-125">Aggiornamento della tabella di aggiornamento per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-125">Updating Upgrade Table for an Upgrade</span></span>](updating-upgrade-table-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-126">Aggiornamento delle proprietà per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-126">Updating Properties for an Upgrade</span></span>](updating-properties-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-127">Aggiornamento di tabelle di sequenza per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-127">Updating Sequence Tables for an Upgrade</span></span>](updating-sequence-tables-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-128">Aggiornamento delle informazioni di riepilogo per un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2e28d-128">Updating Summary Information for an Upgrade</span></span>](updating-summary-information-for-an-upgrade.md)

    [<span data-ttu-id="2e28d-129">Convalida di un aggiornamento dell'installazione</span><span class="sxs-lookup"><span data-stu-id="2e28d-129">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)

 

 



