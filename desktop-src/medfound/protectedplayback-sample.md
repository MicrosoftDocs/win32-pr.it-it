---
description: Viene illustrato come riprodurre contenuto multimediale protetto in Microsoft Media Foundation.
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: Esempio ProtectedPlayback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee64b2a64ce4d40b6f15c2e5afb3b9a39e84c619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753903"
---
# <a name="protectedplayback-sample"></a><span data-ttu-id="8278e-103">Esempio ProtectedPlayback</span><span class="sxs-lookup"><span data-stu-id="8278e-103">ProtectedPlayback Sample</span></span>

<span data-ttu-id="8278e-104">Viene illustrato come riprodurre contenuto multimediale protetto in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8278e-104">Shows how to play protected media content in Microsoft Media Foundation.</span></span>

## <a name="usage"></a><span data-ttu-id="8278e-105">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8278e-105">Usage</span></span>

<span data-ttu-id="8278e-106">L'esempio ProtectedPlayback compila un'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="8278e-106">The ProtectedPlayback sample builds a Windows application.</span></span>

<span data-ttu-id="8278e-107">Per riprodurre un file multimediale locale, scegliere **Apri file** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="8278e-107">To play a local media file, select **Open File** from the **File** menu.</span></span> <span data-ttu-id="8278e-108">Per specificare un file in base all'URL, selezionare **Apri URL** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="8278e-108">To specify a file by URL, select **Open URL** from the **File** menu.</span></span> <span data-ttu-id="8278e-109">Dopo aver selezionato un file, la riproduzione viene avviata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8278e-109">After you select a file, playback begins automatically.</span></span> <span data-ttu-id="8278e-110">Per sospendere la riproduzione, premere la barra SPAZIAtrice.</span><span class="sxs-lookup"><span data-stu-id="8278e-110">To pause playback, press the SPACEBAR.</span></span> <span data-ttu-id="8278e-111">Per riprendere la riproduzione, premere di nuovo la barra SPAZIAtrice.</span><span class="sxs-lookup"><span data-stu-id="8278e-111">To resume playback, press the SPACEBAR again.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="8278e-112">API illustrate</span><span class="sxs-lookup"><span data-stu-id="8278e-112">APIs Demonstrated</span></span>

<span data-ttu-id="8278e-113">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="8278e-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="8278e-114">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="8278e-114">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [<span data-ttu-id="8278e-115">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="8278e-115">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a><span data-ttu-id="8278e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8278e-116">Requirements</span></span>



| <span data-ttu-id="8278e-117">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8278e-117">Product</span></span>                                                        | <span data-ttu-id="8278e-118">Versione</span><span class="sxs-lookup"><span data-stu-id="8278e-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="8278e-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8278e-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="8278e-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8278e-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="8278e-121">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="8278e-121">Downloading the Sample</span></span>

<span data-ttu-id="8278e-122">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span><span class="sxs-lookup"><span data-stu-id="8278e-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8278e-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8278e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8278e-124">Come riprodurre file multimediali protetti</span><span class="sxs-lookup"><span data-stu-id="8278e-124">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="8278e-125">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="8278e-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

<span data-ttu-id="8278e-126">[Esempio MFPlayer](/previous-versions//bb970516(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8278e-126">[MFPlayer Sample](/previous-versions//bb970516(v=vs.85))</span></span>
</dt> </dl>

 

 
