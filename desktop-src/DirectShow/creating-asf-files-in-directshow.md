---
description: Creazione di file ASF in DirectShow
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Creazione di file ASF in DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f5c9ebac0b14b736c47599ee25a1c1c28dd8f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304320"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="fc01d-103">Creazione di file ASF in DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="fc01d-103">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="fc01d-104">In questa sezione viene descritto come utilizzare il filtro di scrittura di DirectShow [WM ASF](wm-asf-writer-filter.md) per creare file in formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="fc01d-104">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="fc01d-105">ASF è un formato contenitore che può contenere qualsiasi tipo di dati compressi o non compressi.</span><span class="sxs-lookup"><span data-stu-id="fc01d-105">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="fc01d-106">I file di formato Windows Media sono file ASF che usano determinati codec, come specificato in Windows Media Format Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fc01d-106">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="fc01d-107">Questi file usano le estensioni "WMA" per i file di Windows Media Audio e ". wmv" per i file di Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="fc01d-107">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="fc01d-108">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc01d-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="fc01d-109">DirectShow SDK e Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="fc01d-109">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="fc01d-110">Configurazione del writer ASF</span><span class="sxs-lookup"><span data-stu-id="fc01d-110">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="fc01d-111">Creazione di grafici filtro per la scrittura di file ASF</span><span class="sxs-lookup"><span data-stu-id="fc01d-111">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="fc01d-112">Configurazione di profili e altre proprietà dei file ASF</span><span class="sxs-lookup"><span data-stu-id="fc01d-112">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="fc01d-113">Sblocco di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="fc01d-113">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="fc01d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc01d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc01d-115">Uso di Windows Media in DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc01d-115">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



