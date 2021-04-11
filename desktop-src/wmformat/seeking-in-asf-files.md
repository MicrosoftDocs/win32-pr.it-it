---
title: Ricerca nei file ASF (Windows Media Format 11 SDK)
description: Ricerca nei file ASF
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, ricerca nei file ASF
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Formato Advanced Systems (ASF), ricerca
- ASF (formato avanzato dei sistemi), ricerca
- DirectShow, ricerca nei file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047689"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="50057-110">Ricerca nei file ASF (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="50057-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="50057-111">Il [lettore WM ASF](wm-asf-reader-filter.md), tramite la relativa interfaccia **IMediaSeeking** , può eseguire ricerche temporali molto accurate sul contenuto basato su Windows Media con un indice temporale.</span><span class="sxs-lookup"><span data-stu-id="50057-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="50057-112">(Tutti i contenuti indicizzati con frame contengono anche un indice temporale). La ricerca con precisione dei frame garantita non è supportata direttamente nel lettore di WM ASF, ma esiste un modo per eseguire questa operazione se questa funzionalità è necessaria.</span><span class="sxs-lookup"><span data-stu-id="50057-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="50057-113">In primo luogo, usare direttamente Windows Media Format SDK per creare un'istanza dell'oggetto Reader sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia DirectShow **IMediaSeeking** per cercare tale orario.</span><span class="sxs-lookup"><span data-stu-id="50057-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="50057-114">L'interfaccia DirectShow **IVideoFrameStep** non supporta la ricerca con frame accurato di contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50057-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="50057-115">L'esempio DSSeekFm in Windows Media Format SDK illustra come eseguire la ricerca con precisione dei frame usando il lettore WM ASF.</span><span class="sxs-lookup"><span data-stu-id="50057-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50057-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50057-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50057-117">**Filtro di lettura ASF WM**</span><span class="sxs-lookup"><span data-stu-id="50057-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




