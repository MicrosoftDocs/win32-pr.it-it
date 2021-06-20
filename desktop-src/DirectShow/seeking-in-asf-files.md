---
description: Informazioni su come WM ASF Reader può eseguire una ricerca temporale molto accurata su contenuto basato su Windows Media con un indice temporale in DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Ricerca nei file ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405584"
---
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="aa271-103">Ricerca nei file ASF (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="aa271-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="aa271-104">Il [lettore ASF WM,](wm-asf-reader-filter.md)tramite la relativa [**interfaccia IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) può eseguire una ricerca temporale molto accurata su contenuto basato su Windows Media con un indice temporale.</span><span class="sxs-lookup"><span data-stu-id="aa271-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="aa271-105">Tutto il contenuto indicizzato con frame contiene anche un indice temporale. La ricerca con accuratezza dei frame garantita non è supportata direttamente nel lettore ASF WM, ma è possibile farlo se è necessaria questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="aa271-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="aa271-106">Usare prima di tutto Windows Media Format SDK direttamente per creare un'istanza dell'oggetto lettore sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia DirectShow **IMediaSeeking** per cercare tale ora.</span><span class="sxs-lookup"><span data-stu-id="aa271-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="aa271-107">[**L'interfaccia IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) non supporta la ricerca accurata dei frame del contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="aa271-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa271-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa271-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa271-109">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa271-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



