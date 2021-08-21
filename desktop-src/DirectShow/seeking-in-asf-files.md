---
description: Informazioni su come WM ASF Reader può eseguire una ricerca temporale molto accurata Windows contenuto basato su Media con un indice temporale in DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Ricerca nei file ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1bea9749b80b15072efe29a749bd7312de865514ce597f1ec1584dca5cf139c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951950"
---
# <a name="seeking-in-asf-files-directshow"></a>Ricerca nei file ASF (DirectShow)

[Wm ASF Reader,](wm-asf-reader-filter.md)tramite la relativa [**interfaccia IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) può eseguire una ricerca temporale molto accurata Windows contenuto basato su media con un indice temporale. Tutto il contenuto indicizzato con frame contiene anche un indice temporale. La ricerca con accuratezza dei frame garantita non è supportata direttamente nel lettore ASF WM, ma è possibile farlo se è necessaria questa funzionalità. Usare prima di tutto Windows Media Format SDK per creare un'istanza dell'oggetto lettore sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia **IMediaSeeking** di DirectShow per cercare tale ora. [**L'interfaccia IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) non supporta la ricerca con frame accurato Windows contenuto basato su supporti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



