---
description: Questo esempio illustra come creare un semplice pacchetto di Windows Installer per l'installazione di un'applicazione.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Esempio di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881137"
---
# <a name="an-installation-example"></a><span data-ttu-id="291e7-103">Esempio di installazione</span><span class="sxs-lookup"><span data-stu-id="291e7-103">An Installation Example</span></span>

<span data-ttu-id="291e7-104">Questo esempio illustra come creare un semplice pacchetto di Windows Installer per l'installazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="291e7-104">This example illustrates how to create a simple Windows Installer package that installs an application.</span></span> <span data-ttu-id="291e7-105">Nell'esempio viene installato il blocco note, un editor di testo incluso in Windows e diversi file di testo che descrivono gli eventi e le ammissioni nell'Arena Red Park immaginaria.</span><span class="sxs-lookup"><span data-stu-id="291e7-105">The sample installs Notepad, a text editor included with Windows, and several text files describing events and admissions at the imaginary Red Park Arena.</span></span>

<span data-ttu-id="291e7-106">Nell'esempio sono presenti le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="291e7-106">The sample has the following specifications:</span></span>

-   <span data-ttu-id="291e7-107">L'applicazione viene fornita agli utenti come pacchetto di Windows Installer di installazione automatica che installa tutti i file, i collegamenti e le informazioni del registro di sistema necessari.</span><span class="sxs-lookup"><span data-stu-id="291e7-107">The application is provided to users as a self-installing Windows Installer package that installs all the required files, shortcuts, and registry information.</span></span>
-   <span data-ttu-id="291e7-108">Il pacchetto di installazione può presentare all'utente una procedura guidata dell'interfaccia utente durante l'installazione per raccogliere informazioni sull'utente.</span><span class="sxs-lookup"><span data-stu-id="291e7-108">The installation package may present a UI wizard to the user during setup to collect user information.</span></span>
-   <span data-ttu-id="291e7-109">Durante l'installazione, gli utenti hanno la possibilità di selezionare le singole funzionalità da installare per l'esecuzione in locale, l'esecuzione dall'origine o l'installazione.</span><span class="sxs-lookup"><span data-stu-id="291e7-109">During setup, users have the option of selecting individual features to be installed to run-locally, to run-from-source, or to not be installed.</span></span>
-   <span data-ttu-id="291e7-110">Una delle funzionalità può essere presentata agli utenti come una funzionalità di installazione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="291e7-110">One of the features can be presented to users as an install-on-demand feature.</span></span>
-   <span data-ttu-id="291e7-111">Lo stesso pacchetto Disinstalla l'applicazione e rimuove tutti i file dell'applicazione e le informazioni del registro di sistema dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="291e7-111">The same package uninstalls the application and removes all the application files and registry information from the user's computer.</span></span>
-   <span data-ttu-id="291e7-112">Il pacchetto è pronto a ricevere un aggiornamento principale che include la modifica del codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="291e7-112">The package is prepared to receive a major upgrade that includes changing its product code.</span></span>

<span data-ttu-id="291e7-113">Per riprodurre l'esempio, è necessario uno strumento software in grado di creare e modificare un database di Windows Installer vuoto.</span><span class="sxs-lookup"><span data-stu-id="291e7-113">To reproduce the example, you need a software tool capable of creating and editing a blank Windows Installer database.</span></span> <span data-ttu-id="291e7-114">Sono disponibili diversi strumenti per la creazione di pacchetti di fornitori di software indipendenti.</span><span class="sxs-lookup"><span data-stu-id="291e7-114">Several package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="291e7-115">Un editor di database Windows Installer denominato Orca viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="291e7-115">A Windows Installer database editor called Orca is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="291e7-116">Per completare l'esempio, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="291e7-116">To complete the example, follow these steps:</span></span>

[<span data-ttu-id="291e7-117">Pianificazione dell'installazione</span><span class="sxs-lookup"><span data-stu-id="291e7-117">Planning the Installation</span></span>](planning-the-installation.md)

[<span data-ttu-id="291e7-118">Importazione di un database vuoto</span><span class="sxs-lookup"><span data-stu-id="291e7-118">Importing a Blank Database</span></span>](importing-a-blank-database.md)

[<span data-ttu-id="291e7-119">Specifica della struttura di directory</span><span class="sxs-lookup"><span data-stu-id="291e7-119">Specifying Directory Structure</span></span>](specifying-directory-structure.md)

[<span data-ttu-id="291e7-120">Specifica di componenti</span><span class="sxs-lookup"><span data-stu-id="291e7-120">Specifying Components</span></span>](specifying-components.md)

[<span data-ttu-id="291e7-121">Specifica di file e attributi di file</span><span class="sxs-lookup"><span data-stu-id="291e7-121">Specifying Files and File Attributes</span></span>](specifying-files-and-file-attributes.md)

[<span data-ttu-id="291e7-122">Specifica dei supporti di origine</span><span class="sxs-lookup"><span data-stu-id="291e7-122">Specifying Source Media</span></span>](specifying-source-media.md)

[<span data-ttu-id="291e7-123">Specifica delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="291e7-123">Specifying Features</span></span>](specifying-features.md)

[<span data-ttu-id="291e7-124">Specifica di relazioni Feature-Component</span><span class="sxs-lookup"><span data-stu-id="291e7-124">Specifying Feature-Component Relationships</span></span>](specifying-feature-component-relationships.md)

[<span data-ttu-id="291e7-125">Aggiunta di informazioni del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="291e7-125">Adding Registry Information</span></span>](adding-registry-information.md)

[<span data-ttu-id="291e7-126">Specifica dei collegamenti</span><span class="sxs-lookup"><span data-stu-id="291e7-126">Specifying Shortcuts</span></span>](specifying-shortcuts.md)

[<span data-ttu-id="291e7-127">Specifica delle proprietà</span><span class="sxs-lookup"><span data-stu-id="291e7-127">Specifying Properties</span></span>](specifying-properties.md)

[<span data-ttu-id="291e7-128">Importazione del InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="291e7-128">Importing the InstallExecuteSequence</span></span>](importing-the-installexecutesequence.md)

[<span data-ttu-id="291e7-129">Importazione del InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="291e7-129">Importing the InstallUISequence</span></span>](importing-the-installuisequence.md)

[<span data-ttu-id="291e7-130">Importazione del AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="291e7-130">Importing the AdminExecuteSequence</span></span>](importing-the-adminexecutesequence.md)

[<span data-ttu-id="291e7-131">Importazione del AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="291e7-131">Importing the AdminUISequence</span></span>](importing-the-adminuisequence.md)

[<span data-ttu-id="291e7-132">Importazione del AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="291e7-132">Importing the AdvtExecuteSequence</span></span>](importing-the-advtexecutesequence.md)

[<span data-ttu-id="291e7-133">Aggiunta di informazioni di riepilogo</span><span class="sxs-lookup"><span data-stu-id="291e7-133">Adding Summary Information</span></span>](adding-summary-information.md)

[<span data-ttu-id="291e7-134">Importazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="291e7-134">Importing the User Interface</span></span>](importing-the-user-interface.md)

[<span data-ttu-id="291e7-135">Convalida di un database di installazione</span><span class="sxs-lookup"><span data-stu-id="291e7-135">Validating an Installation Database</span></span>](validating-an-installation-database.md)

 

 



