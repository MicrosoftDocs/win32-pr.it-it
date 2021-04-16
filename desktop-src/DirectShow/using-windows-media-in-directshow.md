---
description: Uso di Windows Media in DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Uso di Windows Media in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104401828"
---
# <a name="using-windows-media-in-directshow"></a><span data-ttu-id="8da21-103">Uso di Windows Media in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8da21-103">Using Windows Media in DirectShow</span></span>

<span data-ttu-id="8da21-104">In questa sezione viene descritto come utilizzare DirectShow per riprodurre e scrivere file con estensione ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="8da21-104">This section describes how to use DirectShow to play and write Advanced Systems Format (ASF) files.</span></span> <span data-ttu-id="8da21-105">I file ASF contengono in genere contenuti audio e video codificati con i codec Windows Media Audio e video.</span><span class="sxs-lookup"><span data-stu-id="8da21-105">ASF files commonly contain audio and video content encoded using the Windows Media Audio and Video codecs.</span></span> <span data-ttu-id="8da21-106">Tuttavia, ASF può contenere qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="8da21-106">However, ASF can contain any type of data.</span></span>

<span data-ttu-id="8da21-107">I filtri DirectShow seguenti supportano la lettura e la scrittura di file ASF:</span><span class="sxs-lookup"><span data-stu-id="8da21-107">The following DirectShow filters support reading and writing ASF files:</span></span>

-   <span data-ttu-id="8da21-108">[Filtro di lettura ASF WM](wm-asf-reader-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8da21-108">[WM ASF Reader Filter](wm-asf-reader-filter.md).</span></span> <span data-ttu-id="8da21-109">Legge i file ASF.</span><span class="sxs-lookup"><span data-stu-id="8da21-109">Reads ASF files.</span></span>
-   <span data-ttu-id="8da21-110">[Filtro del writer ASF WM](wm-asf-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8da21-110">[WM ASF Writer Filter](wm-asf-writer-filter.md).</span></span> <span data-ttu-id="8da21-111">File ASF Wrties.</span><span class="sxs-lookup"><span data-stu-id="8da21-111">Wrties ASF files.</span></span>
-   <span data-ttu-id="8da21-112">[Filtro wrapper DMO](dmo-wrapper-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8da21-112">[DMO Wrapper Filter](dmo-wrapper-filter.md).</span></span> <span data-ttu-id="8da21-113">Esegue il wrapping del codificatore Windows Media e del decodificatore DMOs.</span><span class="sxs-lookup"><span data-stu-id="8da21-113">Wraps the Windows Media encoder and decoder DMOs.</span></span>

### <a name="versions"></a><span data-ttu-id="8da21-114">Versioni</span><span class="sxs-lookup"><span data-stu-id="8da21-114">Versions</span></span>

<span data-ttu-id="8da21-115">I filtri WM ASF Reader e WM ASF Writer sono inclusi nella DLL denominata qasf.dll e i filtri sono collettivamente denominati "QASF Components".</span><span class="sxs-lookup"><span data-stu-id="8da21-115">The WM ASF Reader and WM ASF Writer filters are packaged in the DLL named qasf.dll, and the filters are collectively named "QASF components."</span></span> <span data-ttu-id="8da21-116">Questi filtri sono wrapper per Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="8da21-116">These filters are wrappers for the Windows Media Format SDK.</span></span> <span data-ttu-id="8da21-117">La DLL (qasf.dll) è stata pubblicata per la prima volta in DirectX SDK, ma in seguito è stata aggiornata in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="8da21-117">The DLL (qasf.dll) was first published in the DirectX SDK but was later updated in the Windows Media Format SDK.</span></span> <span data-ttu-id="8da21-118">Ecco la cronologia delle versioni dei filtri QASF:</span><span class="sxs-lookup"><span data-stu-id="8da21-118">Here is the version history of the QASF filters:</span></span>

-   <span data-ttu-id="8da21-119">DirectShow 8,1 supporta Windows Media Format SDK versione 7,0.</span><span class="sxs-lookup"><span data-stu-id="8da21-119">DirectShow 8.1 supports Windows Media Format SDK version 7.0.</span></span>
-   <span data-ttu-id="8da21-120">DirectShow 9,0 supporta Windows Media Format SDK versione 7,1.</span><span class="sxs-lookup"><span data-stu-id="8da21-120">DirectShow 9.0 supports Windows Media Format SDK version 7.1.</span></span>
-   <span data-ttu-id="8da21-121">Windows XP Service Pack 2 supporta Windows Media Format 9 SDK.</span><span class="sxs-lookup"><span data-stu-id="8da21-121">Windows XP Service Pack 2 supports Windows Media Format 9 SDK.</span></span>
-   <span data-ttu-id="8da21-122">Windows Vista supporta Windows Media Format 11 SDK.</span><span class="sxs-lookup"><span data-stu-id="8da21-122">Windows Vista supports Windows Media Format 11 SDK.</span></span>
-   <span data-ttu-id="8da21-123">Windows Media Format 9 SDK e versioni successive contengono versioni corrispondenti di QASF.</span><span class="sxs-lookup"><span data-stu-id="8da21-123">Windows Media Format 9 SDK and later contain corresponding versions of QASF.</span></span>

<span data-ttu-id="8da21-124">Per ottenere la versione più recente di QASF, scaricare sempre la versione più recente di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="8da21-124">To get the latest version of QASF, always download the latest Windows Media Format SDK.</span></span>

### <a name="legacy-windows-media-source-filter"></a><span data-ttu-id="8da21-125">Filtro origine Windows Media legacy</span><span class="sxs-lookup"><span data-stu-id="8da21-125">Legacy Windows Media Source Filter</span></span>

<span data-ttu-id="8da21-126">In Windows XP Service Pack 1 e versioni precedenti, il filtro di origine predefinito per i file ASF (con estensione ASF, WMV e WMA) è il filtro di [origine Windows Media](windows-media-source-filter.md)obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8da21-126">In Windows XP Service Pack 1 and earlier, the default source filter for ASF files (.asf, .wmv, and .wma file extensions) is the obsolete [Windows Media Source Filter](windows-media-source-filter.md).</span></span> <span data-ttu-id="8da21-127">Questo comportamento è stato mantenuto per garantire la compatibilità con le applicazioni che usavano Windows Media Player 6,4.</span><span class="sxs-lookup"><span data-stu-id="8da21-127">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="8da21-128">Le nuove applicazioni devono usare le versioni più recenti di QASF, che fanno in modo che il lettore WM ASF filtri il filtro predefinito per la riproduzione di file ASF.</span><span class="sxs-lookup"><span data-stu-id="8da21-128">New applications should use the newer versions of QASF, which make the WM ASF Reader filter the default filter for playing ASF files.</span></span>

<span data-ttu-id="8da21-129">Per ulteriori informazioni su Windows Media Suite di Software Development Kit, vedere la sezione [audio e video](../audio-and-video.md) della libreria MDSN.</span><span class="sxs-lookup"><span data-stu-id="8da21-129">For more information on the Windows Media suite of software development kits, see the [Audio and Video](../audio-and-video.md) section of the MDSN Library.</span></span>

<span data-ttu-id="8da21-130">Questo articolo contiene gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8da21-130">This article contains the following topics:</span></span>

-   [<span data-ttu-id="8da21-131">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8da21-131">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
-   [<span data-ttu-id="8da21-132">Creazione di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8da21-132">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="8da21-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8da21-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8da21-134">Uso di DirectShow</span><span class="sxs-lookup"><span data-stu-id="8da21-134">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 
