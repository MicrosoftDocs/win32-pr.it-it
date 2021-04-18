---
description: Questo argomento descrive come compilare una tipica applicazione MUI.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizzazione delle risorse e compilazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308704"
---
# <a name="localizing-resources-and-building-the-application"></a><span data-ttu-id="af8d5-103">Localizzazione delle risorse e compilazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="af8d5-103">Localizing Resources and Building the Application</span></span>

<span data-ttu-id="af8d5-104">Questo argomento descrive come compilare una tipica applicazione MUI.</span><span class="sxs-lookup"><span data-stu-id="af8d5-104">This topic describes how to build a typical MUI application.</span></span> <span data-ttu-id="af8d5-105">Si presuppone che si stiano usando Microsoft Visual Studio per la codifica e Microsoft Visual Studio o la riga di comando di Visual Studio per la compilazione.</span><span class="sxs-lookup"><span data-stu-id="af8d5-105">It is assumed that you are using Microsoft Visual Studio for coding and either Microsoft Visual Studio or the Visual Studio command line for building.</span></span> <span data-ttu-id="af8d5-106">Si presuppone l'utilizzo di un file di soluzione con estensione sln per l'applicazione e il supporto di un file Resource. h per riflettere il file di risorse della lingua di base.</span><span class="sxs-lookup"><span data-stu-id="af8d5-106">You are assumed to use an .sln solution file for your application and support a Resource.h file to reflect the base language resource file.</span></span>

> [!Note]  
> <span data-ttu-id="af8d5-107">Se si usa la riga di comando di Visual Studio per la compilazione, si userà il comando **VCBuild** per compilare il file di soluzione.</span><span class="sxs-lookup"><span data-stu-id="af8d5-107">If using the Visual Studio command line for the build, you will use the **vcbuild** command to build the solution file.</span></span>

 

<span data-ttu-id="af8d5-108">I file dell'applicazione vengono compilati separatamente per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="af8d5-108">Application files are built separately for each language.</span></span> <span data-ttu-id="af8d5-109">Ogni compilazione crea file con estensione exe, indipendenti dalla lingua e file. exe. mui specifici della lingua.</span><span class="sxs-lookup"><span data-stu-id="af8d5-109">Each build creates identical language-neutral .exe and language-specific .exe.mui files.</span></span> <span data-ttu-id="af8d5-110">Inoltre, diversi altri file vengono copiati nelle cartelle della versione appropriate.</span><span class="sxs-lookup"><span data-stu-id="af8d5-110">In addition, various other files are copied to the appropriate release folders.</span></span>

<span data-ttu-id="af8d5-111">La compilazione dell'applicazione dipende dal tipo di risorse e dal tipo di localizzazione utilizzato.</span><span class="sxs-lookup"><span data-stu-id="af8d5-111">The application build depends on the type of resources and the type of localization that you are using.</span></span> <span data-ttu-id="af8d5-112">Per la localizzazione pre-compilazione, è presente una copia del file della lingua di base localizzata per ogni lingua supportata.</span><span class="sxs-lookup"><span data-stu-id="af8d5-112">For pre-build localization, you have one copy of the base language file localized for each supported language.</span></span> <span data-ttu-id="af8d5-113">Per la localizzazione post-compilazione, è possibile copiare il file con estensione MUI risultante dalla compilazione del modulo eseguibile e risorse e fornire le copie ai localizzatori.</span><span class="sxs-lookup"><span data-stu-id="af8d5-113">For post-build localization, you can copy the .mui file resulting from the build of the executable and resource module, and provide the copies to the localizers.</span></span>

> [!Note]  
> <span data-ttu-id="af8d5-114">Nella procedura seguente si presuppone che le risorse PE Win32 con un progetto di Visual Studio siano compilate per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="af8d5-114">The following procedure assumes Win32 PE resources with one Visual Studio project built for each language.</span></span> <span data-ttu-id="af8d5-115">Le risorse della lingua di base vengono fornite in un file RC e caricate tramite un modulo DLL.</span><span class="sxs-lookup"><span data-stu-id="af8d5-115">The base language resources are provided in an .rc file and loaded using a DLL module.</span></span> <span data-ttu-id="af8d5-116">È possibile ripetere la procedura in base alle esigenze per la compilazione per tutte le lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="af8d5-116">You can repeat the procedure as needed to build for all languages supported.</span></span>

 

<span data-ttu-id="af8d5-117">**Per compilare l'applicazione**</span><span class="sxs-lookup"><span data-stu-id="af8d5-117">**To build the application**</span></span>

1.  <span data-ttu-id="af8d5-118">Configurare un progetto di Visual Studio per la lingua di base.</span><span class="sxs-lookup"><span data-stu-id="af8d5-118">Set up a Visual Studio project for the base language.</span></span>
2.  <span data-ttu-id="af8d5-119">Se si è interessati all'uso di un file di configurazione delle risorse con gli strumenti di risorse, impostarne uno come descritto in [preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="af8d5-119">If interested in using a resource configuration file with the resource tools, set one up as described in [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>
3.  <span data-ttu-id="af8d5-120">Impostare i parametri richiesti dall'utilità del compilatore RC nelle pagine delle proprietà del progetto in **proprietà di configurazione → risorse → riga di comando → opzioni aggiuntive**.</span><span class="sxs-lookup"><span data-stu-id="af8d5-120">Set parameters required by the RC Compiler utility in the property pages for the project under **Configuration Properties → Resources → Command Line → Additional options**.</span></span>
4.  <span data-ttu-id="af8d5-121">Eseguire il compilatore RC.</span><span class="sxs-lookup"><span data-stu-id="af8d5-121">Run RC Compiler.</span></span> <span data-ttu-id="af8d5-122">L'utilità compila e suddivide le risorse non localizzabili e localizzabili in due file oggetto diversi, usando i dati di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="af8d5-122">The utility compiles and splits the non-localizable and localizable resources into two different object files, using resource configuration data.</span></span> <span data-ttu-id="af8d5-123">In questo passaggio le risorse indipendenti dalla lingua sono collegate a un file in.</span><span class="sxs-lookup"><span data-stu-id="af8d5-123">In this step the language-neutral resources are linked into an LN file.</span></span> <span data-ttu-id="af8d5-124">Per ulteriori informazioni, vedere la descrizione dell'utilità in [Utilità risorse](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="af8d5-124">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
5.  <span data-ttu-id="af8d5-125">Per collegare le risorse specifiche della lingua in un file con estensione MUI specifico della lingua, impostare un evento di post-compilazione per il progetto nelle pagine delle proprietà in **proprietà di configurazione → eventi di compilazione → evento post-compilazione → riga di comando**.</span><span class="sxs-lookup"><span data-stu-id="af8d5-125">To link the language-specific resources into a language-specific .mui file, set a post-build event for the project in the property pages under **Configuration Properties → Build Events → Post-Build Event → Command Line**.</span></span>
6.  <span data-ttu-id="af8d5-126">Impostare un evento di post-compilazione per applicare il valore di checksum dal file LN al file con estensione MUI per la lingua.</span><span class="sxs-lookup"><span data-stu-id="af8d5-126">Set a post-build event to apply the checksum value from the LN file to the .mui file for the language.</span></span> <span data-ttu-id="af8d5-127">È possibile usare l'utilità MUIRCT per questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="af8d5-127">You can use the MUIRCT utility for this step.</span></span> <span data-ttu-id="af8d5-128">Per ulteriori informazioni, vedere la descrizione dell'utilità in [Utilità risorse](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="af8d5-128">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
7.  <span data-ttu-id="af8d5-129">Utilizzare la riga di comando eventi post-compilazione per aggiungere comandi per copiare i file nella struttura di cartelle della versione appropriata.</span><span class="sxs-lookup"><span data-stu-id="af8d5-129">Use the post-build event command line to add commands to copy the files into the appropriate release folder structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af8d5-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af8d5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af8d5-131">Uso dell'interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="af8d5-131">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="af8d5-132">Preparazione di un file di configurazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="af8d5-132">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="af8d5-133">Utilità per le risorse</span><span class="sxs-lookup"><span data-stu-id="af8d5-133">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



