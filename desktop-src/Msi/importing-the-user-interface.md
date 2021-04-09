---
description: Oltre alle informazioni illustrate nelle sezioni precedenti, uisample.msi contiene anche i dati per un'interfaccia utente di esempio.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importazione dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879682"
---
# <a name="importing-the-user-interface"></a><span data-ttu-id="a47a8-103">Importazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a47a8-103">Importing the User Interface</span></span>

<span data-ttu-id="a47a8-104">Oltre alle informazioni illustrate nelle sezioni precedenti, uisample.msi contiene anche i dati per un'interfaccia utente di esempio.</span><span class="sxs-lookup"><span data-stu-id="a47a8-104">In addition to information discussed in previous sections, uisample.msi also contains data for a sample user interface.</span></span> <span data-ttu-id="a47a8-105">Se è stato eseguito il merge uisample.msi in MNP2000.msi nella sezione [importazione di un database vuoto](importing-a-blank-database.md), queste informazioni sono presenti anche in MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="a47a8-105">If you merged uisample.msi into MNP2000.msi in the section [Importing a Blank Database](importing-a-blank-database.md), then this information is present in MNP2000.msi as well.</span></span> <span data-ttu-id="a47a8-106">Le informazioni per l'interfaccia utente di esempio sono incluse nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="a47a8-106">The information for the sample user interface is in the following tables.</span></span>

-   [<span data-ttu-id="a47a8-107">Tabella ActionText</span><span class="sxs-lookup"><span data-stu-id="a47a8-107">ActionText table</span></span>](actiontext-table.md)
-   [<span data-ttu-id="a47a8-108">Tabella binaria</span><span class="sxs-lookup"><span data-stu-id="a47a8-108">Binary table</span></span>](binary-table.md)
-   [<span data-ttu-id="a47a8-109">Tabella di controllo</span><span class="sxs-lookup"><span data-stu-id="a47a8-109">Control table</span></span>](control-table.md)
-   [<span data-ttu-id="a47a8-110">Tabella ControlEvent</span><span class="sxs-lookup"><span data-stu-id="a47a8-110">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="a47a8-111">Tabella finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="a47a8-111">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="a47a8-112">Tabella degli errori</span><span class="sxs-lookup"><span data-stu-id="a47a8-112">Error table</span></span>](error-table.md)
-   [<span data-ttu-id="a47a8-113">Tabella EventMapping</span><span class="sxs-lookup"><span data-stu-id="a47a8-113">EventMapping table</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="a47a8-114">RadioButton (tabella)</span><span class="sxs-lookup"><span data-stu-id="a47a8-114">RadioButton table</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="a47a8-115">Tabella TextStyle</span><span class="sxs-lookup"><span data-stu-id="a47a8-115">TextStyle table</span></span>](textstyle-table.md)
-   [<span data-ttu-id="a47a8-116">Tabella UIText</span><span class="sxs-lookup"><span data-stu-id="a47a8-116">UIText table</span></span>](uitext-table.md)

<span data-ttu-id="a47a8-117">L'orca dell'editor di database fornito con il programma di installazione include un'opzione di anteprima della finestra di dialogo che è possibile usare per visualizzare in anteprima le finestre di dialogo dell'interfaccia utente specificata dai dati nelle tabelle precedenti.</span><span class="sxs-lookup"><span data-stu-id="a47a8-117">The database editor Orca provided with the installer includes a dialog preview option that you can use to preview the dialogs of the user interface that is specified by the data in the above tables.</span></span>

<span data-ttu-id="a47a8-118">Il pacchetto di installazione di esempio MNP2000.msi è ora pronto per la convalida del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a47a8-118">The sample installation package MNP2000.msi is now ready for package validation.</span></span> <span data-ttu-id="a47a8-119">Eseguire sempre la convalida in un nuovo pacchetto prima di tentare di installare il pacchetto per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="a47a8-119">Always run validation on a new package before attempting to install the package for the first time.</span></span> <span data-ttu-id="a47a8-120">Questa operazione viene illustrata in convalida dell'esempio di installazione.</span><span class="sxs-lookup"><span data-stu-id="a47a8-120">This is discussed in Validating the Installation Sample.</span></span>

<span data-ttu-id="a47a8-121">Se non si desidera includere l'interfaccia utente nel pacchetto di esempio, omettere o rimuovere tutte le informazioni nelle tabelle riportate in precedenza, ad eccezione della [tabella TextStyle](textstyle-table.md) (necessaria per definire la proprietà [**DefaultUIFont**](defaultuifont.md) ).</span><span class="sxs-lookup"><span data-stu-id="a47a8-121">If you do not want to include the user interface in the sample package, omit or remove the all information in the tables shown above except for the [TextStyle table](textstyle-table.md) (which is needed to define the [**DefaultUIFont**](defaultuifont.md) property).</span></span> <span data-ttu-id="a47a8-122">È inoltre necessario rimuovere le proprietà dell'interfaccia utente dalla [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="a47a8-122">You should also remove user interface properties from the [Property Table](property-table.md).</span></span> <span data-ttu-id="a47a8-123">Di seguito è riportata una tabella delle proprietà di esempio per l'esempio del blocco note, senza interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a47a8-123">An example Property table for the Notepad sample, without a UI, is shown below.</span></span> <span data-ttu-id="a47a8-124">Se si copia questo esempio, non riutilizzare i GUID visualizzati nella tabella.</span><span class="sxs-lookup"><span data-stu-id="a47a8-124">Do not reuse the GUIDs shown in the table if you copy this example.</span></span>

[<span data-ttu-id="a47a8-125">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="a47a8-125">Property Table</span></span>](property-table.md)



| <span data-ttu-id="a47a8-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a47a8-126">Property</span></span>                                   | <span data-ttu-id="a47a8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a47a8-127">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="a47a8-128">**DefaultUIFont**</span><span class="sxs-lookup"><span data-stu-id="a47a8-128">**DefaultUIFont**</span></span>](defaultuifont.md)     | <span data-ttu-id="a47a8-129">DlgFont8</span><span class="sxs-lookup"><span data-stu-id="a47a8-129">DlgFont8</span></span>                               |
| [<span data-ttu-id="a47a8-130">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="a47a8-130">**INSTALLLEVEL**</span></span>](installlevel.md)       | <span data-ttu-id="a47a8-131">3</span><span class="sxs-lookup"><span data-stu-id="a47a8-131">3</span></span>                                      |
| [<span data-ttu-id="a47a8-132">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="a47a8-132">**LIMITUI**</span></span>](limitui.md)                 | <span data-ttu-id="a47a8-133">1</span><span class="sxs-lookup"><span data-stu-id="a47a8-133">1</span></span>                                      |
| [<span data-ttu-id="a47a8-134">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="a47a8-134">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="a47a8-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="a47a8-135">Microsoft</span></span>                              |
| [<span data-ttu-id="a47a8-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="a47a8-136">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="a47a8-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="a47a8-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> |
| [<span data-ttu-id="a47a8-138">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="a47a8-138">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="a47a8-139">1033</span><span class="sxs-lookup"><span data-stu-id="a47a8-139">1033</span></span>                                   |
| [<span data-ttu-id="a47a8-140">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="a47a8-140">**ProductName**</span></span>](productname.md)         | <span data-ttu-id="a47a8-141">MNP2000</span><span class="sxs-lookup"><span data-stu-id="a47a8-141">MNP2000</span></span>                                |
| [<span data-ttu-id="a47a8-142">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="a47a8-142">**ProductVersion**</span></span>](productversion.md)   | <span data-ttu-id="a47a8-143">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="a47a8-143">01.40.0000</span></span>                             |
| [<span data-ttu-id="a47a8-144">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="a47a8-144">**UpgradeCode**</span></span>](upgradecode.md)         | <span data-ttu-id="a47a8-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="a47a8-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> |



 

<span data-ttu-id="a47a8-146">Un pacchetto senza un'interfaccia utente può essere installato dalla riga di comando o da un programma.</span><span class="sxs-lookup"><span data-stu-id="a47a8-146">A package without a user interface can be installed from the command line or from a program.</span></span> <span data-ttu-id="a47a8-147">Per installare un pacchetto dalla riga di comando, usare i metodi descritti in [Opzioni della riga di comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="a47a8-147">To install a package from the command line use the methods described in [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="a47a8-148">Per installare un pacchetto da un programma, utilizzare i metodi descritti in [utilizzo delle funzioni di installazione](using-installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a47a8-148">To install a package from a program use the methods described in [Using Installer Functions](using-installer-functions.md).</span></span> <span data-ttu-id="a47a8-149">Eseguire sempre la convalida in un nuovo pacchetto prima di tentare di installare un nuovo pacchetto per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="a47a8-149">Always run validation on a new package before attempting to install a new package for the first time.</span></span>

[<span data-ttu-id="a47a8-150">Continua</span><span class="sxs-lookup"><span data-stu-id="a47a8-150">Continue</span></span>](validating-an-installation-database.md)

 

 



