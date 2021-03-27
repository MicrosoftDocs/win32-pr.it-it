---
description: Illustra le sovrapposizioni e le barre di stato dell'icona della barra delle applicazioni.
title: Esempio di stato della periferica della barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995045"
---
# <a name="taskbar-peripheral-status-sample"></a><span data-ttu-id="5ec11-103">Esempio di stato della periferica della barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="5ec11-103">Taskbar Peripheral Status Sample</span></span>

<span data-ttu-id="5ec11-104">Illustra le sovrapposizioni e le barre di stato dell'icona della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5ec11-104">Demonstrates taskbar icon overlays and progress bars.</span></span>

<span data-ttu-id="5ec11-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ec11-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5ec11-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec11-106">Description</span></span>](#description)
-   [<span data-ttu-id="5ec11-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ec11-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5ec11-108">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5ec11-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="5ec11-109">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5ec11-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="5ec11-110">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5ec11-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="5ec11-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ec11-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="5ec11-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec11-112">Description</span></span>

<span data-ttu-id="5ec11-113">Questo esempio crea un pulsante della barra delle applicazioni di esempio in cui viene illustrato l'uso di [**all'ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) consentendo di applicare varie sovrimpressioni scelte da un menu.</span><span class="sxs-lookup"><span data-stu-id="5ec11-113">This sample creates an example taskbar button on which it demonstrates the use of [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) by allowing you to apply various overlays chosen from a menu.</span></span>

<span data-ttu-id="5ec11-114">L'esempio fornisce anche la possibilità di simulare un indicatore di stato sul pulsante, dimostrando l'uso di [**all'ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) e [**all'ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) mostrando inizialmente un indicatore di stato indeterminato (TBPF \_ indeterminato), quindi un indicatore proporzionale normale (TBPF \_ normale).</span><span class="sxs-lookup"><span data-stu-id="5ec11-114">The sample also provides the option of simulating a progress indicator on the button, demonstrating the use of [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) and [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) by showing at first an indeterminate progress indicator (TBPF\_INDETERMINATE), and then a normal proportional indicator (TBPF\_NORMAL).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ec11-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ec11-115">Requirements</span></span>



| <span data-ttu-id="5ec11-116">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5ec11-116">Product</span></span>                                | <span data-ttu-id="5ec11-117">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="5ec11-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="5ec11-118">Windows</span><span class="sxs-lookup"><span data-stu-id="5ec11-118">Windows</span></span>                                | <span data-ttu-id="5ec11-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ec11-119">Windows 7</span></span>               |
| <span data-ttu-id="5ec11-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="5ec11-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="5ec11-121">7.0</span><span class="sxs-lookup"><span data-stu-id="5ec11-121">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="5ec11-122">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5ec11-122">Downloading the Sample</span></span>

| <span data-ttu-id="5ec11-123">Location</span><span class="sxs-lookup"><span data-stu-id="5ec11-123">Location</span></span>      | <span data-ttu-id="5ec11-124">URL percorso</span><span class="sxs-lookup"><span data-stu-id="5ec11-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec11-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="5ec11-125">GitHub</span></span>  | [<span data-ttu-id="5ec11-126">Esempio TaskBarPeripheralStatus</span><span class="sxs-lookup"><span data-stu-id="5ec11-126">TaskBarPeripheralStatus sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a><span data-ttu-id="5ec11-127">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5ec11-127">Building the Sample</span></span>

<span data-ttu-id="5ec11-128">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="5ec11-128">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="5ec11-129">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="5ec11-129">Open the command prompt window and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="5ec11-130">Immettere `msbuild PeripheralStatus.sln`.</span><span class="sxs-lookup"><span data-stu-id="5ec11-130">Enter `msbuild PeripheralStatus.sln`.</span></span>

<span data-ttu-id="5ec11-131">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="5ec11-131">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="5ec11-132">Aprire Esplora risorse e passare alla directory del progetto **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="5ec11-132">Open Windows Explorer and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="5ec11-133">Fare doppio clic sull'icona per il file PeripheralStatus. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5ec11-133">Double-click the icon for the PeripheralStatus.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="5ec11-134">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="5ec11-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="5ec11-135">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5ec11-135">Running the Sample</span></span>

1.  <span data-ttu-id="5ec11-136">Passare alla directory che contiene il nuovo file eseguibile (ad esempio, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), usando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="5ec11-136">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="5ec11-137">Se si usa la riga di comando, immettere `PeripheralStatus.exe` .</span><span class="sxs-lookup"><span data-stu-id="5ec11-137">If using the command line, enter `PeripheralStatus.exe`.</span></span>
    -   <span data-ttu-id="5ec11-138">Se si usa Esplora risorse, fare doppio clic sull'icona per PeripheralStatus.exe.</span><span class="sxs-lookup"><span data-stu-id="5ec11-138">If using Windows Explorer, double-click the icon for PeripheralStatus.exe.</span></span>

    <span data-ttu-id="5ec11-139">Viene aperta una nuova finestra con un pulsante della barra delle applicazioni associato.</span><span class="sxs-lookup"><span data-stu-id="5ec11-139">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="5ec11-140">Per dimostrare le sovrapposizioni, scegliere **sovrimpressione 1** o **sovrapposizione 2** dal menu **stato periferica** della finestra.</span><span class="sxs-lookup"><span data-stu-id="5ec11-140">To demonstrate overlays, choose **Overlay 1** or **Overlay 2** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="5ec11-141">La sovrimpressione scelta verrà visualizzata sul pulsante della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5ec11-141">The chosen overlay appears on the taskbar button.</span></span> <span data-ttu-id="5ec11-142">Per rimuovere la sovrimpressione, scegliere **Cancella sovrimpressione**.</span><span class="sxs-lookup"><span data-stu-id="5ec11-142">To remove the overlay, choose **Clear Overlay**.</span></span>
3.  <span data-ttu-id="5ec11-143">Per illustrare l'indicatore di stato, scegliere **simula stato** dal menu **stato periferica** della finestra.</span><span class="sxs-lookup"><span data-stu-id="5ec11-143">To demonstrate the progress bar, choose **Simulate Progress** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="5ec11-144">Il pulsante della barra delle applicazioni Visualizza un indicatore di stato indeterminato, quindi passa a un indicatore normale.</span><span class="sxs-lookup"><span data-stu-id="5ec11-144">The taskbar button will show an indeterminate progress indicator then switch to a normal indicator.</span></span>
4.  <span data-ttu-id="5ec11-145">Scegliere **Esci** dal menu **file** della finestra per terminare il programma.</span><span class="sxs-lookup"><span data-stu-id="5ec11-145">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ec11-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ec11-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec11-147">Estensioni della barra delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="5ec11-147">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



