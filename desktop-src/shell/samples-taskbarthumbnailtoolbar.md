---
description: Viene illustrata una barra degli strumenti dell'anteprima, un controllo attivo della barra degli strumenti incorporato nell'anteprima dell'anteprima di una finestra, usato per fornire l'accesso ai comandi chiave di una finestra senza fare in modo che l'utente ripristini o attivi la finestra dell'applicazione.
title: Esempio di barra degli strumenti di anteprima della barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980322"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a><span data-ttu-id="b76b8-103">Esempio di barra degli strumenti di anteprima della barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="b76b8-103">Taskbar Thumbnail Toolbar Sample</span></span>

<span data-ttu-id="b76b8-104">Viene illustrata una barra degli strumenti dell'anteprima, un controllo attivo della barra degli strumenti incorporato nell'anteprima dell'anteprima di una finestra, usato per fornire l'accesso ai comandi chiave di una finestra senza fare in modo che l'utente ripristini o attivi la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b76b8-104">Demonstrates a thumbnail toolbar, an active toolbar control embedded in a window's thumbnail preview, used to provide access to a window's key commands without making the user restore or activate the application's window.</span></span>

<span data-ttu-id="b76b8-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b76b8-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b76b8-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b76b8-106">Description</span></span>](#description)
-   [<span data-ttu-id="b76b8-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b76b8-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b76b8-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76b8-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b76b8-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76b8-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b76b8-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76b8-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="b76b8-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b76b8-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b76b8-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b76b8-112">Description</span></span>

<span data-ttu-id="b76b8-113">In questo esempio viene illustrato come fornire una semplice barra degli strumenti per un'anteprima dell'anteprima della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b76b8-113">This sample shows how to provide a simple toolbar to a taskbar thumbnail preview.</span></span> <span data-ttu-id="b76b8-114">La barra degli strumenti è costituita da tre pulsanti.</span><span class="sxs-lookup"><span data-stu-id="b76b8-114">The toolbar consists of three buttons.</span></span> <span data-ttu-id="b76b8-115">Quando si fa clic su un pulsante, viene visualizzata una finestra per confermare che il pulsante è stato attivato.</span><span class="sxs-lookup"><span data-stu-id="b76b8-115">Clicking a button displays a window to confirm that the button was activated.</span></span> <span data-ttu-id="b76b8-116">Vengono illustrate le API seguenti:</span><span class="sxs-lookup"><span data-stu-id="b76b8-116">The following APIs are demonstrated:</span></span>

-   [<span data-ttu-id="b76b8-117">**All'ITaskbarList3:: ThumbBarAddButtons**</span><span class="sxs-lookup"><span data-stu-id="b76b8-117">**ITaskbarList3::ThumbBarAddButtons**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [<span data-ttu-id="b76b8-118">**All'ITaskbarList3:: ThumbBarSetImageList**</span><span class="sxs-lookup"><span data-stu-id="b76b8-118">**ITaskbarList3::ThumbBarSetImageList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   <span data-ttu-id="b76b8-119">Struttura [**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)</span><span class="sxs-lookup"><span data-stu-id="b76b8-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) structure</span></span>

## <a name="requirements"></a><span data-ttu-id="b76b8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b76b8-120">Requirements</span></span>



| <span data-ttu-id="b76b8-121">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b76b8-121">Product</span></span>                                | <span data-ttu-id="b76b8-122">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="b76b8-122">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="b76b8-123">Windows</span><span class="sxs-lookup"><span data-stu-id="b76b8-123">Windows</span></span>                                | <span data-ttu-id="b76b8-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b76b8-124">Windows 7</span></span>               |
| <span data-ttu-id="b76b8-125">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="b76b8-125">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="b76b8-126">7.0</span><span class="sxs-lookup"><span data-stu-id="b76b8-126">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b76b8-127">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76b8-127">Downloading the Sample</span></span>

| <span data-ttu-id="b76b8-128">Location</span><span class="sxs-lookup"><span data-stu-id="b76b8-128">Location</span></span>      | <span data-ttu-id="b76b8-129">URL percorso</span><span class="sxs-lookup"><span data-stu-id="b76b8-129">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b76b8-130">GitHub</span><span class="sxs-lookup"><span data-stu-id="b76b8-130">GitHub</span></span>  | [<span data-ttu-id="b76b8-131">Esempio TaskbarThumbnailToolbar</span><span class="sxs-lookup"><span data-stu-id="b76b8-131">TaskbarThumbnailToolbar sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a><span data-ttu-id="b76b8-132">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76b8-132">Building the Sample</span></span>

<span data-ttu-id="b76b8-133">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="b76b8-133">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="b76b8-134">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="b76b8-134">Open the command prompt window and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="b76b8-135">Immettere `msbuild ThumbnailToolbar.sln`.</span><span class="sxs-lookup"><span data-stu-id="b76b8-135">Enter `msbuild ThumbnailToolbar.sln`.</span></span>

<span data-ttu-id="b76b8-136">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="b76b8-136">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="b76b8-137">Aprire Esplora risorse e passare alla directory del progetto **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="b76b8-137">Open Windows Explorer and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="b76b8-138">Fare doppio clic sull'icona per il file ThumbnailToolbar. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b76b8-138">Double-click the icon for the ThumbnailToolbar.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="b76b8-139">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="b76b8-139">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b76b8-140">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="b76b8-140">Running the Sample</span></span>

1.  <span data-ttu-id="b76b8-141">Passare alla directory che contiene il nuovo file eseguibile (ad esempio, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), usando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="b76b8-141">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="b76b8-142">Se si usa la riga di comando, immettere `ThumbnailToolbar.exe` .</span><span class="sxs-lookup"><span data-stu-id="b76b8-142">If using the command line, enter `ThumbnailToolbar.exe`.</span></span>
    -   <span data-ttu-id="b76b8-143">Se si usa Esplora risorse, fare doppio clic sull'icona per ThumbnailToolbar.exe.</span><span class="sxs-lookup"><span data-stu-id="b76b8-143">If using Windows Explorer, double-click the icon for ThumbnailToolbar.exe.</span></span>

    <span data-ttu-id="b76b8-144">Viene aperta una nuova finestra con un pulsante della barra delle applicazioni associato.</span><span class="sxs-lookup"><span data-stu-id="b76b8-144">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="b76b8-145">Posizionare il puntatore del mouse sul pulsante della barra delle applicazioni di **ThumbnailToolbar** in modo che l'anteprima venga visualizzata.</span><span class="sxs-lookup"><span data-stu-id="b76b8-145">Hover the cursor over the **ThumbnailToolbar** taskbar button so that the preview displays.</span></span> <span data-ttu-id="b76b8-146">Fare clic su uno dei tre pulsanti (verde, giallo, rosso) visualizzato sulla barra degli strumenti dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="b76b8-146">Click one of the three buttons (green, yellow, red) shown in the preview's toolbar.</span></span>
3.  <span data-ttu-id="b76b8-147">Scegliere **Esci** dal menu **file** della finestra per terminare il programma.</span><span class="sxs-lookup"><span data-stu-id="b76b8-147">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b76b8-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b76b8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b76b8-149">Estensioni della barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="b76b8-149">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



