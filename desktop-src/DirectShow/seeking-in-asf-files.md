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
# <a name="seeking-in-asf-files-directshow"></a>Ricerca nei file ASF (DirectShow)

Il [lettore ASF WM,](wm-asf-reader-filter.md)tramite la relativa [**interfaccia IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) può eseguire una ricerca temporale molto accurata su contenuto basato su Windows Media con un indice temporale. Tutto il contenuto indicizzato con frame contiene anche un indice temporale. La ricerca con accuratezza dei frame garantita non è supportata direttamente nel lettore ASF WM, ma è possibile farlo se è necessaria questa funzionalità. Usare prima di tutto Windows Media Format SDK direttamente per creare un'istanza dell'oggetto lettore sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia DirectShow **IMediaSeeking** per cercare tale ora. [**L'interfaccia IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) non supporta la ricerca accurata dei frame del contenuto basato su Windows Media.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



