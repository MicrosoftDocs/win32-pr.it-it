---
description: Informazioni sulla creazione di file ASF in DirectShow. ASF è un formato contenitore che può contenere qualsiasi tipo di dati.
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Creazione di file ASF in DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4614ed813c2e9f51c77cd8773739188aa5d4d07
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403965"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="dc044-104">Creazione di file ASF in DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="dc044-104">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="dc044-105">Questa sezione descrive come usare il filtro DirectShow [WM ASF Writer](wm-asf-writer-filter.md) per creare file in Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="dc044-105">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="dc044-106">ASF è un formato contenitore che può contenere qualsiasi tipo di dati compressi o non compressi.</span><span class="sxs-lookup"><span data-stu-id="dc044-106">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="dc044-107">I file di formato Windows Media sono file ASF che usano determinati codec come specificato in Windows Media Format Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="dc044-107">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="dc044-108">Questi file usano le estensioni ".wma" per Windows Media Audio e ".wmv" per Windows Media Video file.</span><span class="sxs-lookup"><span data-stu-id="dc044-108">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="dc044-109">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc044-109">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="dc044-110">DirectShow SDK e Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="dc044-110">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="dc044-111">Configurazione di ASF Writer</span><span class="sxs-lookup"><span data-stu-id="dc044-111">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="dc044-112">Compilazione di grafici filtro per la scrittura di file ASF</span><span class="sxs-lookup"><span data-stu-id="dc044-112">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="dc044-113">Configurazione di profili e altre proprietà dei file ASF</span><span class="sxs-lookup"><span data-stu-id="dc044-113">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="dc044-114">Sblocco di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="dc044-114">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="dc044-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc044-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc044-116">Uso di Windows Media in DirectShow</span><span class="sxs-lookup"><span data-stu-id="dc044-116">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



