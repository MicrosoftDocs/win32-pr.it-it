---
title: Ricerca nei file ASF (Windows Media Format 11 SDK)
description: Informazioni su come WM ASF Reader può eseguire una ricerca temporale molto accurata su contenuto basato su Windows Media con un indice temporale in Windows Media Format 11 SDK.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, ricerca nei file ASF
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format),DirectShow
- Advanced Systems Format (ASF), ricerca
- ASF (Advanced Systems Format), ricerca
- DirectShow, ricerca nei file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807631861cdc820457360058f22fca380fca29ea
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409884"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="d6abc-110">Ricerca nei file ASF (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="d6abc-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="d6abc-111">[Wm ASF Reader,](wm-asf-reader-filter.md)tramite l'interfaccia **IMediaSeeking,** può eseguire una ricerca temporale molto accurata sul contenuto basato su Windows Media con un indice temporale.</span><span class="sxs-lookup"><span data-stu-id="d6abc-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="d6abc-112">Tutto il contenuto indicizzato con frame contiene anche un indice temporale. La ricerca con accuratezza dei frame garantita non è supportata direttamente nel lettore ASF WM, ma esiste un modo per farlo se è necessaria questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d6abc-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="d6abc-113">Usare innanzitutto Windows Media Format SDK direttamente per creare un'istanza dell'oggetto lettore sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia **DirectShow IMediaSeeking** per cercare tale ora.</span><span class="sxs-lookup"><span data-stu-id="d6abc-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="d6abc-114">L'interfaccia **DirectShow IVideoFrameStep** non supporta la ricerca accurata dei frame del contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d6abc-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="d6abc-115">L'esempio DSSeekFm in Windows Media Format SDK illustra come eseguire una ricerca accurata dei frame usando wm asf reader.</span><span class="sxs-lookup"><span data-stu-id="d6abc-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6abc-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6abc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6abc-117">**Filtro lettore ASF WM**</span><span class="sxs-lookup"><span data-stu-id="d6abc-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




