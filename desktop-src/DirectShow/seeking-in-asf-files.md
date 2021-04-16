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
# <a name="seeking-in-asf-files-directshow"></a>Ricerca nei file ASF (DirectShow)

Il [lettore WM ASF](wm-asf-reader-filter.md), tramite la relativa interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , può eseguire ricerche temporali molto accurate sul contenuto basato su Windows Media con un indice temporale. (Tutti i contenuti indicizzati con frame contengono anche un indice temporale). La ricerca con precisione dei frame garantita non è supportata direttamente nel lettore di WM ASF, ma esiste un modo per eseguire questa operazione se questa funzionalità è necessaria. In primo luogo, usare direttamente Windows Media Format SDK per creare un'istanza dell'oggetto Reader sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia DirectShow **IMediaSeeking** per cercare tale orario. L'interfaccia [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) non supporta la ricerca con frame accurato di contenuto basato su Windows Media.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



