---
description: In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un file di immagine e Direct2D per eseguire il rendering dell'immagine sullo schermo.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visualizzatore immagini WIC con esempio Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323889"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a><span data-ttu-id="c68a4-103">Visualizzatore immagini WIC con esempio Direct2D</span><span class="sxs-lookup"><span data-stu-id="c68a4-103">WIC image viewer using Direct2D sample</span></span>

<span data-ttu-id="c68a4-104">In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un file di immagine e Direct2D per eseguire il rendering dell'immagine sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="c68a4-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image file and Direct2D to render the image to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68a4-105">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c68a4-105">Requirements</span></span>

<span data-ttu-id="c68a4-106">Questo esempio presenta i requisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="c68a4-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="c68a4-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="c68a4-107">Requirement</span></span> | <span data-ttu-id="c68a4-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c68a4-108">Value</span></span> |
|-|-|
| <span data-ttu-id="c68a4-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c68a4-109">Minimum supported client</span></span> | <span data-ttu-id="c68a4-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c68a4-110">Windows Vista</span></span> |
| <span data-ttu-id="c68a4-111">Windows SDK minimo</span><span class="sxs-lookup"><span data-stu-id="c68a4-111">Minimum Windows SDK</span></span> | <span data-ttu-id="c68a4-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per Windows 7</span><span class="sxs-lookup"><span data-stu-id="c68a4-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="c68a4-113">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c68a4-113">Downloading the sample</span></span>

<span data-ttu-id="c68a4-114">Questo esempio è disponibile nel [Visualizzatore WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span><span class="sxs-lookup"><span data-stu-id="c68a4-114">This sample is available at [WIC Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c68a4-115">Compilare l'esempio</span><span class="sxs-lookup"><span data-stu-id="c68a4-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="c68a4-116">Uso di Visual Studio (metodo preferito)</span><span class="sxs-lookup"><span data-stu-id="c68a4-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="c68a4-117">Aprire Esplora risorse, quindi spostarsi nella directory.</span><span class="sxs-lookup"><span data-stu-id="c68a4-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="c68a4-118">Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il file in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c68a4-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="c68a4-119">Scegliere **Compila soluzione** dal menu **Compila**.</span><span class="sxs-lookup"><span data-stu-id="c68a4-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="c68a4-120">L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c68a4-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="c68a4-121">Tramite il prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="c68a4-121">Using the command prompt</span></span>

<span data-ttu-id="c68a4-122">Per compilare l'esempio utilizzando un prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="c68a4-122">To build the sample by using a command prompt:</span></span>

1. <span data-ttu-id="c68a4-123">Aprire una finestra del prompt dei comandi e passare alla directory di esempio.</span><span class="sxs-lookup"><span data-stu-id="c68a4-123">Open a command prompt window and navigate to the sample directory.</span></span>
2. <span data-ttu-id="c68a4-124">Digitare `msbuild WICViewerD2D.sln`</span><span class="sxs-lookup"><span data-stu-id="c68a4-124">Type `msbuild WICViewerD2D.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c68a4-125">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c68a4-125">Running the sample</span></span>

<span data-ttu-id="c68a4-126">Dopo aver avviato l'applicazione, caricare un file di immagine usando il comando **Apri** del menu **file** .</span><span class="sxs-lookup"><span data-stu-id="c68a4-126">After you start the application, load an image file by using the **Open** command of the **File** menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="c68a4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c68a4-127">See also</span></span>

[<span data-ttu-id="c68a4-128">Codec Microsoft Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c68a4-128">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="c68a4-129">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="c68a4-129">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="c68a4-130">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c68a4-130">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="c68a4-131">Direct2D</span><span class="sxs-lookup"><span data-stu-id="c68a4-131">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="c68a4-132">Esempi ed esempi di codice</span><span class="sxs-lookup"><span data-stu-id="c68a4-132">Samples and code examples</span></span>](-wic-samples.md)
