---
title: Come sviluppare un'app OEM che usa un file personalizzato
description: Informazioni su come sviluppare un'app che usa un file personalizzato per passare le informazioni dall'OEM all'app.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299588"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a><span data-ttu-id="14e64-103">Come sviluppare un'app OEM che usa un file personalizzato</span><span class="sxs-lookup"><span data-stu-id="14e64-103">How to develop an OEM app that uses a custom file</span></span>

<span data-ttu-id="14e64-104">Per altre informazioni sulla creazione e l'uso di file di dati personalizzati, vedere [Opzioni di Command-Line manutenzione del pacchetto dell'app DISM (con estensione appx o appxbundle)](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span><span class="sxs-lookup"><span data-stu-id="14e64-104">For more information on creating and using custom data files, see [DISM App Package (.appx or .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).</span></span>

<span data-ttu-id="14e64-105">Informazioni su come sviluppare un'app che usa un file personalizzato per passare le informazioni dall'OEM all'app.</span><span class="sxs-lookup"><span data-stu-id="14e64-105">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>

<span data-ttu-id="14e64-106">Per le app create per la distribuzione OEM, è possibile usare un file personalizzato per passare le informazioni dall'OEM alle app.</span><span class="sxs-lookup"><span data-stu-id="14e64-106">For apps that you create for OEM deployment, you can use a custom file to pass info from the OEM to the apps.</span></span> <span data-ttu-id="14e64-107">Per passare le informazioni OEM a un'app, creare un file. data personalizzato nella cartella microsoft.system. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="14e64-107">To pass OEM info to an app, you create a Custom.data file in the microsoft.system.package.metadata folder.</span></span> <span data-ttu-id="14e64-108">Questo nome file è speciale per il sistema operativo e viene eseguito automaticamente durante gli aggiornamenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="14e64-108">This file name is special to the operating system and is automatically carried forward during operating system updates.</span></span> <span data-ttu-id="14e64-109">Gli OEM possono usare questo file per passare gli identificatori personalizzati, in modo che le app sappiano quando gli OEM li hanno distribuiti.</span><span class="sxs-lookup"><span data-stu-id="14e64-109">OEMs can use this file to pass in custom identifiers, so that apps know when OEMs have deployed them.</span></span> <span data-ttu-id="14e64-110">È possibile avere un solo file. data personalizzato per app.</span><span class="sxs-lookup"><span data-stu-id="14e64-110">You can have only one Custom.data file per app.</span></span> <span data-ttu-id="14e64-111">Le app devono essere in grado di cercare e leggere correttamente questo file.</span><span class="sxs-lookup"><span data-stu-id="14e64-111">Apps must be able to look for and read this file correctly.</span></span> <span data-ttu-id="14e64-112">Gli sviluppatori considerano il file come dati non attendibili.</span><span class="sxs-lookup"><span data-stu-id="14e64-112">Developers treat the file as untrusted data.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="14e64-113">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="14e64-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="14e64-114">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="14e64-114">Technologies</span></span>

-   [<span data-ttu-id="14e64-115">Guida introduttiva: informazioni sul manifesto del pacchetto dell'app</span><span class="sxs-lookup"><span data-stu-id="14e64-115">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a><span data-ttu-id="14e64-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="14e64-116">Prerequisites</span></span>

-   <span data-ttu-id="14e64-117">Per aggiungere il pacchetto dell'app con il file di dati personalizzato, è necessario lo strumento [gestione e manutenzione immagini distribuzione (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) .</span><span class="sxs-lookup"><span data-stu-id="14e64-117">You need the [Deployment Image Servicing and Management (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool to add the app package with the custom data file.</span></span>

## <a name="instructions"></a><span data-ttu-id="14e64-118">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="14e64-118">Instructions</span></span>

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a><span data-ttu-id="14e64-119">Passaggio 1: creare un file personalizzato e aggiungerlo alla cartella dei metadati del pacchetto</span><span class="sxs-lookup"><span data-stu-id="14e64-119">Step 1: Create custom file and add it to the package metadata folder</span></span>

<span data-ttu-id="14e64-120">È possibile progettare l'applicazione in modo da usare qualsiasi formato scelto per i dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="14e64-120">You can design your app to use any format you choose for the custom data.</span></span> <span data-ttu-id="14e64-121">È ad esempio possibile usare XML, un file di testo o un altro tipo di file per organizzare i dati.</span><span class="sxs-lookup"><span data-stu-id="14e64-121">For example, you can use XML, a text file, or another file type to organize your data.</span></span> <span data-ttu-id="14e64-122">Si consiglia di considerare come è possibile testare e convalidare il file.</span><span class="sxs-lookup"><span data-stu-id="14e64-122">We recommend that you consider how you can test and validate the file.</span></span> <span data-ttu-id="14e64-123">Ad esempio, è possibile creare un XML Schema per convalidare un file XML.</span><span class="sxs-lookup"><span data-stu-id="14e64-123">For example, you can create an XML schema to validate an XML file.</span></span>

<span data-ttu-id="14e64-124">È possibile specificare qualsiasi tipo di file con qualsiasi nome file per i dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="14e64-124">You can specify any type of file with any file name for the custom data.</span></span> <span data-ttu-id="14e64-125">Quando si aggiunge il pacchetto dell'app con il file di dati personalizzato utilizzando lo strumento [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , DISM Rinomina il file personalizzato in Custom. Data e lo salva nella cartella microsoft.system. Package. Metadata.</span><span class="sxs-lookup"><span data-stu-id="14e64-125">When you add the app package with the custom data file by using the [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) tool, DISM renames the custom file to Custom.data and saves the file to the microsoft.system.package.metadata folder.</span></span>

> [!Note]  
> <span data-ttu-id="14e64-126">Il file di dati personalizzato non può essere modificato dall'app.</span><span class="sxs-lookup"><span data-stu-id="14e64-126">The custom data file can't be modified by the app.</span></span> <span data-ttu-id="14e64-127">Si tratta di una risorsa di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="14e64-127">It's a read-only resource.</span></span>

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a><span data-ttu-id="14e64-128">Passaggio 2: accedere al file di dati personalizzato per un'app</span><span class="sxs-lookup"><span data-stu-id="14e64-128">Step 2: Access the custom data file for an app</span></span>

<span data-ttu-id="14e64-129">È possibile accedere al file Custom. Data per un'app dal codice usando le API di Windows per ottenere informazioni per il pacchetto corrente.</span><span class="sxs-lookup"><span data-stu-id="14e64-129">You can access the Custom.data file for an app from your code by using Windows APIs to get information for the current package.</span></span> <span data-ttu-id="14e64-130">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="14e64-130">For example:</span></span>

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

<span data-ttu-id="14e64-131">Per altre informazioni sullo sviluppo con la proprietà [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , vedere [Guida introduttiva: informazioni sul manifesto del pacchetto dell'app](how-to-query-package-identity-information.md).</span><span class="sxs-lookup"><span data-stu-id="14e64-131">For more info about developing with the [**Package.Current**](/uwp/api/windows.applicationmodel.package.current) property, see [Quickstart: Query app package manifest info](how-to-query-package-identity-information.md).</span></span>

<span data-ttu-id="14e64-132">Per ulteriori informazioni sull'accesso al file Custom. Data tramite [**IStorageFolder. getFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) e l'utilizzo di oggetti [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , vedere [accesso a dati e file](/previous-versions/windows/apps/hh464959(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="14e64-132">For more info about accessing the custom.data file via [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) and by using [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) objects, see [Accessing data and files](/previous-versions/windows/apps/hh464959(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14e64-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14e64-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14e64-134">Guida introduttiva: informazioni sul manifesto del pacchetto dell'app</span><span class="sxs-lookup"><span data-stu-id="14e64-134">Quickstart: Query app package manifest info</span></span>](how-to-query-package-identity-information.md)
</dt> </dl>

 

 