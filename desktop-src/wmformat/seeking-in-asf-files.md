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
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Ricerca nei file ASF (Windows Media Format 11 SDK)

Il [lettore WM ASF](wm-asf-reader-filter.md), tramite la relativa interfaccia **IMediaSeeking** , può eseguire ricerche temporali molto accurate sul contenuto basato su Windows Media con un indice temporale. (Tutti i contenuti indicizzati con frame contengono anche un indice temporale). La ricerca con precisione dei frame garantita non è supportata direttamente nel lettore di WM ASF, ma esiste un modo per eseguire questa operazione se questa funzionalità è necessaria. In primo luogo, usare direttamente Windows Media Format SDK per creare un'istanza dell'oggetto Reader sincrono, aprire il file, ottenere il timestamp associato a un frame specificato e quindi usare l'interfaccia DirectShow **IMediaSeeking** per cercare tale orario. L'interfaccia DirectShow **IVideoFrameStep** non supporta la ricerca con frame accurato di contenuto basato su Windows Media. L'esempio DSSeekFm in Windows Media Format SDK illustra come eseguire la ricerca con precisione dei frame usando il lettore WM ASF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Filtro di lettura ASF WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




