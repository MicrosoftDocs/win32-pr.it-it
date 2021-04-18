---
description: Questo esempio illustra la decodifica di diversi frame in un file GIF, la lettura dei metadati appropriati per ogni frame, la composizione di frame e il rendering dell'animazione con Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Esempio GIF animato WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323894"
---
# <a name="wic-animated-gif-sample"></a><span data-ttu-id="cf43e-103">Esempio GIF animato WIC</span><span class="sxs-lookup"><span data-stu-id="cf43e-103">WIC animated GIF sample</span></span>

<span data-ttu-id="cf43e-104">Questo esempio illustra la decodifica di diversi frame in un file GIF, la lettura dei metadati appropriati per ogni frame, la composizione di frame e il rendering dell'animazione con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cf43e-104">This sample demonstrates decoding various frames in a GIF file, reading appropriate metadata for each frame, composing frames, and rendering the animation with Direct2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf43e-105">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf43e-105">Requirements</span></span>

<span data-ttu-id="cf43e-106">Questo esempio presenta i requisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="cf43e-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="cf43e-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf43e-107">Requirement</span></span> | <span data-ttu-id="cf43e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cf43e-108">Value</span></span> |
|-|-|
| <span data-ttu-id="cf43e-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf43e-109">Minimum supported client</span></span> | <span data-ttu-id="cf43e-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf43e-110">Windows 7</span></span> |
| <span data-ttu-id="cf43e-111">Windows SDK minimo</span><span class="sxs-lookup"><span data-stu-id="cf43e-111">Minimum Windows SDK</span></span> | <span data-ttu-id="cf43e-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf43e-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="cf43e-113">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cf43e-113">Downloading the sample</span></span>

<span data-ttu-id="cf43e-114">Questo esempio è disponibile nel formato [gif animato di WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span><span class="sxs-lookup"><span data-stu-id="cf43e-114">This sample is available at [WIC animated GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="cf43e-115">Compilare l'esempio</span><span class="sxs-lookup"><span data-stu-id="cf43e-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="cf43e-116">Uso di Visual Studio (metodo preferito)</span><span class="sxs-lookup"><span data-stu-id="cf43e-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="cf43e-117">Aprire Esplora risorse, quindi spostarsi nella directory.</span><span class="sxs-lookup"><span data-stu-id="cf43e-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="cf43e-118">Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il file in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cf43e-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="cf43e-119">Scegliere **Compila soluzione** dal menu **Compila**.</span><span class="sxs-lookup"><span data-stu-id="cf43e-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="cf43e-120">L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cf43e-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="cf43e-121">Tramite il prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="cf43e-121">Using the command prompt</span></span>

<span data-ttu-id="cf43e-122">Per compilare l'esempio utilizzando un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="cf43e-122">To build the sample by using a command prompt.</span></span>

1. <span data-ttu-id="cf43e-123">Aprire il prompt dei comandi e passare alla directory di esempio.</span><span class="sxs-lookup"><span data-stu-id="cf43e-123">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="cf43e-124">Digitare `msbuild WICAnimatedGif.sln`</span><span class="sxs-lookup"><span data-stu-id="cf43e-124">Type `msbuild WICAnimatedGif.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cf43e-125">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="cf43e-125">Running the sample</span></span>

<span data-ttu-id="cf43e-126">Dopo l'avvio dell'applicazione, caricare un file di immagine usando il comando **Apri** del menu **file** .</span><span class="sxs-lookup"><span data-stu-id="cf43e-126">After the application is launched, load an image file by using the **Open** command of the **File** menu.</span></span> <span data-ttu-id="cf43e-127">Il ridimensionamento delle finestre è supportato.</span><span class="sxs-lookup"><span data-stu-id="cf43e-127">Window resizing is supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf43e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf43e-128">See also</span></span>

[<span data-ttu-id="cf43e-129">Codec Microsoft Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="cf43e-129">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="cf43e-130">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="cf43e-130">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="cf43e-131">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cf43e-131">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="cf43e-132">Direct2D</span><span class="sxs-lookup"><span data-stu-id="cf43e-132">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="cf43e-133">Esempi ed esempi di codice</span><span class="sxs-lookup"><span data-stu-id="cf43e-133">Samples and code examples</span></span>](-wic-samples.md)
