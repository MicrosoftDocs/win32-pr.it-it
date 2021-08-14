---
title: Ricerca nei file ASF (Windows Media Format 11 SDK)
description: Informazioni su come WM ASF Reader può eseguire una ricerca temporale molto accurata su contenuto basato su Windows Media con un indice temporale in Windows Media Format 11 SDK.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, ricerca nei file ASF
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), ricerca
- ASF (Advanced Systems Format), ricerca
- DirectShow, ricerca nei file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6730f1535c9601cfd0697e374ddfa35b05250ed49fc4b575fa3458b69e389285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845896"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Ricerca nei file ASF (Windows Media Format 11 SDK)

[Wm ASF Reader,](wm-asf-reader-filter.md)tramite l'interfaccia **IMediaSeeking,** può eseguire una ricerca temporale molto accurata Windows contenuto basato su media con un indice temporale. Tutto il contenuto indicizzato con frame contiene anche un indice temporale. La ricerca con accuratezza dei frame garantita non è supportata direttamente nel lettore ASF WM, ma è possibile farlo se è necessaria questa funzionalità. Usare innanzitutto Windows Media Format SDK direttamente per creare un'istanza dell'oggetto lettore sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia **IMediaSeeking** di DirectShow per cercare tale ora. **L DirectShow interfasso IVideoFrameStep** non supporta la ricerca con frame accurato Windows contenuto basato su media. L'esempio DSSeekFm in Windows Media Format SDK illustra come eseguire una ricerca accurata dei frame usando wm asf reader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Filtro lettore ASF WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




