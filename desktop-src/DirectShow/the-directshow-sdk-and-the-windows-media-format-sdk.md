---
description: DirectShow SDK e Windows Media Format SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: DirectShow SDK e Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351661"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a><span data-ttu-id="0ec43-103">DirectShow SDK e Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="0ec43-103">The DirectShow SDK and the Windows Media Format SDK</span></span>

<span data-ttu-id="0ec43-104">DirectShow e Windows Media Format SDK offrono soluzioni complementari per la scrittura di applicazioni per la creazione e la riproduzione di flussi di formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0ec43-104">DirectShow and the Windows Media Format SDK offer complementary solutions for writing applications that create and play back Windows Media Format streams.</span></span> <span data-ttu-id="0ec43-105">Per ulteriori informazioni, vedere la sezione "[audio e video](../audio-and-video.md)" di MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="0ec43-105">For more information, see the "[Audio and Video](../audio-and-video.md)" section of the MSDN Library.</span></span>

<span data-ttu-id="0ec43-106">Il filtro del writer ASF accetta un numero qualsiasi di flussi di input e crea un file ASF.</span><span class="sxs-lookup"><span data-stu-id="0ec43-106">The ASF Writer filter accepts any number of input streams and creates an ASF file.</span></span> <span data-ttu-id="0ec43-107">Il filtro usa Windows Media Format SDK per convertire i file audio o video non compressi in contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0ec43-107">The filter uses the Windows Media Format SDK to convert uncompressed audio or video files to Windows Media-based content.</span></span> <span data-ttu-id="0ec43-108">Il contenuto compresso viene quindi archiviato nel formato del contenitore ASF.</span><span class="sxs-lookup"><span data-stu-id="0ec43-108">The compressed content is then stored in the ASF container format.</span></span> <span data-ttu-id="0ec43-109">Se il contenuto è solo audio, al file viene assegnata un'estensione WMA e viene definito file di Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="0ec43-109">If the content is audio only, then the file is given a .wma extension and is referred to as a Windows Media Audio file.</span></span> <span data-ttu-id="0ec43-110">Se il contenuto è solo video o video e audio, al file viene assegnata un'estensione. WMV e viene definito file di Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="0ec43-110">If the content is video only or video and audio, then the file is given a .wmv extension and is referred to as a Windows Media Video file.</span></span> <span data-ttu-id="0ec43-111">Entrambi i tipi di file possono includere anche i metadati.</span><span class="sxs-lookup"><span data-stu-id="0ec43-111">Either type of file may also include metadata.</span></span>

<span data-ttu-id="0ec43-112">È possibile usare il writer ASF WM in diversi scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di Audio-Video file multimediali con interfoliazione (AVI) o MPEG per lo streaming di rete.</span><span class="sxs-lookup"><span data-stu-id="0ec43-112">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="0ec43-113">Questo filtro rappresenta l'unico modo per creare file di Microsoft® Windows Media™ Audio (WMA) e Windows Media Video (WMV) in DirectShow®.</span><span class="sxs-lookup"><span data-stu-id="0ec43-113">This filter provides the only way to create Microsoft® Windows Media™ Audio (WMA) and Windows Media Video (WMV) files in DirectShow®.</span></span> <span data-ttu-id="0ec43-114">Il filtro può inoltre creare file protetti da Digital Rights Management (DRM) e può anche creare contenuti MPEG-4 usando il codificatore Microsoft MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="0ec43-114">The filter can also create files that are secured by Digital Rights Management (DRM), and can also create MPEG-4 content using the Microsoft MPEG-4 Encoder.</span></span> <span data-ttu-id="0ec43-115">Questo contenuto è archiviato nel formato del contenitore ASF.</span><span class="sxs-lookup"><span data-stu-id="0ec43-115">This content is stored in the ASF container format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ec43-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ec43-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ec43-117">Creazione di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0ec43-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
