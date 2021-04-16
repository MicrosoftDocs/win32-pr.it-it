---
description: Ricerca nei file ASF
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Ricerca nei file ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521289"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="eaddf-103">Ricerca nei file ASF (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="eaddf-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="eaddf-104">Il [lettore WM ASF](wm-asf-reader-filter.md), tramite la relativa interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , può eseguire ricerche temporali molto accurate sul contenuto basato su Windows Media con un indice temporale.</span><span class="sxs-lookup"><span data-stu-id="eaddf-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="eaddf-105">(Tutti i contenuti indicizzati con frame contengono anche un indice temporale). La ricerca con precisione dei frame garantita non è supportata direttamente nel lettore di WM ASF, ma esiste un modo per eseguire questa operazione se questa funzionalità è necessaria.</span><span class="sxs-lookup"><span data-stu-id="eaddf-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="eaddf-106">In primo luogo, usare direttamente Windows Media Format SDK per creare un'istanza dell'oggetto Reader sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia DirectShow **IMediaSeeking** per cercare tale orario.</span><span class="sxs-lookup"><span data-stu-id="eaddf-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="eaddf-107">L'interfaccia [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) non supporta la ricerca con frame accurato di contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="eaddf-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaddf-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaddf-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaddf-109">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="eaddf-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



