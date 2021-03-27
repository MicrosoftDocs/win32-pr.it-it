---
description: Viene illustrato come scrivere un gestore utilizzato per visualizzare un'anteprima del file nel riquadro di anteprima di Esplora risorse o in altri host del gestore di anteprime.
title: Esempio di gestore anteprima file recipe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2C926922-48C0-46f5-8928-67007C6FF957
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05208010c90c7185a777bb75f5de1e67bdb5bc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980247"
---
# <a name="recipe-preview-handler-sample"></a><span data-ttu-id="9b019-103">Esempio di gestore anteprima file recipe</span><span class="sxs-lookup"><span data-stu-id="9b019-103">Recipe Preview Handler Sample</span></span>

<span data-ttu-id="9b019-104">Viene illustrato come scrivere un gestore utilizzato per visualizzare un'anteprima del file nel riquadro di anteprima di Esplora risorse o in altri host del gestore di anteprime.</span><span class="sxs-lookup"><span data-stu-id="9b019-104">Demonstrates how to write a handler used to display a file preview inside the Windows Explorer preview pane or other preview handler hosts.</span></span>

<span data-ttu-id="9b019-105">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b019-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="9b019-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b019-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9b019-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9b019-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9b019-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="9b019-110">Annullamento della registrazione della DLL del gestore di anteprime di esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-110">Unregistering the Sample Preview Handler DLL</span></span>](#unregistering-the-sample-preview-handler-dll)
-   [<span data-ttu-id="9b019-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b019-111">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="9b019-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b019-112">Requirements</span></span>



| <span data-ttu-id="9b019-113">Prodotto</span><span class="sxs-lookup"><span data-stu-id="9b019-113">Product</span></span>                                | <span data-ttu-id="9b019-114">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="9b019-114">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="9b019-115">Windows</span><span class="sxs-lookup"><span data-stu-id="9b019-115">Windows</span></span>                                | <span data-ttu-id="9b019-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b019-116">Windows Vista</span></span>           |
| <span data-ttu-id="9b019-117">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="9b019-117">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="9b019-118">7.0</span><span class="sxs-lookup"><span data-stu-id="9b019-118">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9b019-119">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-119">Downloading the Sample</span></span>

| <span data-ttu-id="9b019-120">Location</span><span class="sxs-lookup"><span data-stu-id="9b019-120">Location</span></span>      | <span data-ttu-id="9b019-121">URL percorso</span><span class="sxs-lookup"><span data-stu-id="9b019-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b019-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="9b019-122">GitHub</span></span>  | [<span data-ttu-id="9b019-123">Esempio RecipePreviewHandler</span><span class="sxs-lookup"><span data-stu-id="9b019-123">RecipePreviewHandler sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/RecipePreviewHandler) |

## <a name="building-the-sample"></a><span data-ttu-id="9b019-124">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-124">Building the Sample</span></span>

<span data-ttu-id="9b019-125">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="9b019-125">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="9b019-126">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="9b019-126">Open the command prompt window and navigate to the **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="9b019-127">Ad esempio: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="9b019-127">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler`.</span></span>
2.  <span data-ttu-id="9b019-128">Immettere `msbuild PreviewHandlerSDKSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="9b019-128">Enter `msbuild PreviewHandlerSDKSample.sln`.</span></span>

<span data-ttu-id="9b019-129">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="9b019-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="9b019-130">Aprire Esplora risorse e passare alla directory del progetto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="9b019-130">Open Windows Explorer and navigate to the **RecipePreviewHandler** project directory.</span></span>
2.  <span data-ttu-id="9b019-131">Fare doppio clic sull'icona per il file PreviewHandlerSDKSample. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9b019-131">Double-click the icon for the PreviewHandlerSDKSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="9b019-132">L'estensione del nome di file sln non viene visualizzata in impostazioni cartella predefinite.</span><span class="sxs-lookup"><span data-stu-id="9b019-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="9b019-133">In tal caso, può essere identificato dalla relativa icona univoca o dalla descrizione del tipo "Microsoft Visual Studio soluzione".</span><span class="sxs-lookup"><span data-stu-id="9b019-133">In that situation, it can be identified by its unique icon or by its type description "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="9b019-134">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="9b019-134">From the **Build** menu, select **Build Solution**.</span></span>

> [!Note]  
> <span data-ttu-id="9b019-135">Se il sistema di destinazione è a 64 bit (x64), questo gestore di anteprime di esempio deve essere compilato come applicazione a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9b019-135">If the target system is 64-bit (x64), this sample preview handler must be built as a 64-bit application.</span></span>

 

## <a name="running-the-sample"></a><span data-ttu-id="9b019-136">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-136">Running the Sample</span></span>

1.  <span data-ttu-id="9b019-137">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **RecipePreviewHandler** compilata.</span><span class="sxs-lookup"><span data-stu-id="9b019-137">Open the command prompt window and navigate to the built **RecipePreviewHandler** project directory.</span></span> <span data-ttu-id="9b019-138">Ad esempio: `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span><span class="sxs-lookup"><span data-stu-id="9b019-138">For example, `C:\Program Files\MicrosoftSDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\RecipePreviewHandler\RecipePreviewHandler`.</span></span> <span data-ttu-id="9b019-139">Immettere `regsvr32.exe PreviewHandlerSDKSample.dll` per registrare il gestore.</span><span class="sxs-lookup"><span data-stu-id="9b019-139">Enter `regsvr32.exe PreviewHandlerSDKSample.dll` to register the handler.</span></span>
2.  <span data-ttu-id="9b019-140">Aprire Esplora risorse e visualizzare il riquadro di anteprima se non è già visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9b019-140">Open Windows Explorer and show the preview pane if it is not already displayed.</span></span>
    -   <span data-ttu-id="9b019-141">**Windows 7**: fare clic sul pulsante anteprima del riquadro.</span><span class="sxs-lookup"><span data-stu-id="9b019-141">**Windows 7**: Click the preview pane button.</span></span>
    -   <span data-ttu-id="9b019-142">**Windows Vista**: fare clic sul menu **organizza** , passare al sottomenu **layout** e selezionare **riquadro di anteprima**.</span><span class="sxs-lookup"><span data-stu-id="9b019-142">**Windows Vista**: Click the **Organize** menu, go to the **Layout** submenu and select **Preview Pane**.</span></span>
3.  <span data-ttu-id="9b019-143">Utilizzare Esplora risorse per passare alla directory del progetto **RecipePreviewHandler** .</span><span class="sxs-lookup"><span data-stu-id="9b019-143">Use Windows Explorer to navigate to the **RecipePreviewHandler** project directory.</span></span>
4.  <span data-ttu-id="9b019-144">Selezionare il file example. recipe.</span><span class="sxs-lookup"><span data-stu-id="9b019-144">Select the example .recipe file.</span></span>

<span data-ttu-id="9b019-145">Per fare in modo che l'output a 32 bit (x86) e 64 bit (x64) funzioni in una versione di Windows a 64 bit, impostare il valore **AppID** sull'host surrogato WOW64 `{534A1E02-D58F-44f0-B58B-36CBED287C7C}` , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="9b019-145">To make both the 32-bit (x86) and 64-bit (x64) output work on a 64-bit version of Windows, set the **AppId** value to the WOW64 surrogate host `{534A1E02-D58F-44f0-B58B-36CBED287C7C}`, as shown in the following code.</span></span>


```
{HKEY_CURRENT_USER,   
 L"Software\\Classes\\CLSID\\" SZ_CLSID_RecipePreviewHandler,
 L"AppID",
 L"{534A1E02-D58F-44f0-B58B-36CBED287C7C}"}
```



## <a name="unregistering-the-sample-preview-handler-dll"></a><span data-ttu-id="9b019-146">Annullamento della registrazione della DLL del gestore di anteprime di esempio</span><span class="sxs-lookup"><span data-stu-id="9b019-146">Unregistering the Sample Preview Handler DLL</span></span>

-   <span data-ttu-id="9b019-147">Aprire la finestra del prompt dei comandi e immettere `regsvr32.exe /u PreviewHandlerSDKSample.dll` per annullare la registrazione del gestore.</span><span class="sxs-lookup"><span data-stu-id="9b019-147">Open the command prompt window and enter `regsvr32.exe /u PreviewHandlerSDKSample.dll` to unregister the handler.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b019-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b019-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b019-149">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="9b019-149">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
</dt> <dt>

[<span data-ttu-id="9b019-150">**IPreviewHandlerFrame**</span><span class="sxs-lookup"><span data-stu-id="9b019-150">**IPreviewHandlerFrame**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe)
</dt> <dt>

[<span data-ttu-id="9b019-151">ID modello utente applicazione (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="9b019-151">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
