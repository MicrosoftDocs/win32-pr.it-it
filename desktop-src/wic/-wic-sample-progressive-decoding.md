---
description: In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un'immagine codificata con livelli progressivi.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Esempio di decodifica progressiva WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323890"
---
# <a name="wic-progressive-decoding-sample"></a><span data-ttu-id="4fac9-103">Esempio di decodifica progressiva WIC</span><span class="sxs-lookup"><span data-stu-id="4fac9-103">WIC progressive decoding sample</span></span>

<span data-ttu-id="4fac9-104">In questo esempio viene illustrato l'utilizzo di Windows Imaging Component (WIC) per decodificare un'immagine codificata con livelli progressivi.</span><span class="sxs-lookup"><span data-stu-id="4fac9-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image that is encoded with progressive levels.</span></span> <span data-ttu-id="4fac9-105">In questo esempio viene utilizzato Direct2D per eseguire il rendering dei diversi livelli progressivi sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="4fac9-105">This sample uses Direct2D to render the different progressive levels to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fac9-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fac9-106">Requirements</span></span>

<span data-ttu-id="4fac9-107">Questo esempio presenta i requisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="4fac9-107">This sample has the following requirements.</span></span>

| <span data-ttu-id="4fac9-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fac9-108">Requirement</span></span> | <span data-ttu-id="4fac9-109">Valore</span><span class="sxs-lookup"><span data-stu-id="4fac9-109">Value</span></span> |
|-|
| <span data-ttu-id="4fac9-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fac9-110">Minimum supported client</span></span> | <span data-ttu-id="4fac9-111">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fac9-111">Windows 7</span></span> |
| <span data-ttu-id="4fac9-112">Windows SDK minimo</span><span class="sxs-lookup"><span data-stu-id="4fac9-112">Minimum Windows SDK</span></span> | <span data-ttu-id="4fac9-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fac9-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="4fac9-114">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="4fac9-114">Downloading the sample</span></span>

<span data-ttu-id="4fac9-115">Questo esempio è disponibile nella [codifica progressiva WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span><span class="sxs-lookup"><span data-stu-id="4fac9-115">This sample is available at [WIC progressive encoding](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="4fac9-116">Compilare l'esempio</span><span class="sxs-lookup"><span data-stu-id="4fac9-116">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="4fac9-117">Uso di Visual Studio (metodo preferito)</span><span class="sxs-lookup"><span data-stu-id="4fac9-117">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="4fac9-118">Aprire Esplora risorse, quindi spostarsi nella directory.</span><span class="sxs-lookup"><span data-stu-id="4fac9-118">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="4fac9-119">Fare doppio clic sull'icona del file con estensione sln (soluzione) per aprire il file in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4fac9-119">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="4fac9-120">Scegliere Genera soluzione dal menu Genera.</span><span class="sxs-lookup"><span data-stu-id="4fac9-120">In the Build menu, select Build Solution.</span></span> <span data-ttu-id="4fac9-121">L'applicazione verrà compilata nella \\ directory di debug o di \\ versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4fac9-121">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="4fac9-122">Tramite il prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="4fac9-122">Using the command prompt</span></span>

<span data-ttu-id="4fac9-123">Per compilare l'esempio utilizzando il prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="4fac9-123">To build the sample using the command prompt.</span></span>

1. <span data-ttu-id="4fac9-124">Aprire il prompt dei comandi e passare alla directory di esempio.</span><span class="sxs-lookup"><span data-stu-id="4fac9-124">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="4fac9-125">Digitare `msbuild WICProgressiveDecoding.sln`</span><span class="sxs-lookup"><span data-stu-id="4fac9-125">Type `msbuild WICProgressiveDecoding.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4fac9-126">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="4fac9-126">Running the sample</span></span>

<span data-ttu-id="4fac9-127">Dopo l'avvio dell'applicazione, caricare un file di immagine tramite il menu file Apri.</span><span class="sxs-lookup"><span data-stu-id="4fac9-127">After the application is launched, load an image file through file open menu.</span></span> <span data-ttu-id="4fac9-128">Al caricamento, il livello progressivo predefinito è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="4fac9-128">On loading, the default progressive level is set to 0.</span></span> <span data-ttu-id="4fac9-129">È possibile passare a livelli progressivi diversi tramite il menu o il tasto freccia su o giù.</span><span class="sxs-lookup"><span data-stu-id="4fac9-129">You can navigate to different progressive levels either through menu or Up/Down key.</span></span> <span data-ttu-id="4fac9-130">Il testo del livello progressivo corrente viene visualizzato sulla barra di stato della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="4fac9-130">The current progressive level text is displayed on the main window status bar.</span></span> <span data-ttu-id="4fac9-131">Il ridimensionamento delle finestre è supportato.</span><span class="sxs-lookup"><span data-stu-id="4fac9-131">Window resizing is supported.</span></span>

> [!NOTE]
> <span data-ttu-id="4fac9-132">La decodifica progressiva è disponibile solo per le immagini che sono state codificate progressivamente.</span><span class="sxs-lookup"><span data-stu-id="4fac9-132">Progressive decoding is available only for images that have been progressively encoded.</span></span> <span data-ttu-id="4fac9-133">L'immagine fornita con questo esempio è stata codificata in maniera progressiva.</span><span class="sxs-lookup"><span data-stu-id="4fac9-133">The image provided with this sample has been progressively encoded.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fac9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fac9-134">See also</span></span>

[<span data-ttu-id="4fac9-135">Codec Microsoft Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="4fac9-135">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="4fac9-136">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="4fac9-136">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="4fac9-137">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4fac9-137">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="4fac9-138">Direct2D</span><span class="sxs-lookup"><span data-stu-id="4fac9-138">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="4fac9-139">Esempi ed esempi di codice</span><span class="sxs-lookup"><span data-stu-id="4fac9-139">Samples and code examples</span></span>](-wic-samples.md)

[<span data-ttu-id="4fac9-140">Panoramica della decodifica progressiva</span><span class="sxs-lookup"><span data-stu-id="4fac9-140">Progressive decoding overview</span></span>](-wic-progressive-decoding.md)
