---
description: Pin delle porte video in Acquisizione file
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Pin delle porte video in Acquisizione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab348c7e378f4130b43eef45f2cf4ddd079b0e85a77397b767cadddde5a7d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049381"
---
# <a name="video-port-pins-in-file-capture"></a>Pin delle porte video in Acquisizione file

Se il dispositivo di acquisizione ha una porta video, il pin della porta video deve essere connesso a un renderer video, anche se si vuole acquisire solo in un file.

Se si chiama [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con il valore **PIN CATEGORY \_ \_ CAPTURE** e il dispositivo ha un pin di porta video, Capture Graph Builder connette automaticamente il pin della porta video al filtro [overlay Mixer](overlay-mixer-filter.md) e connette il Mixer di sovrimpressione al renderer video. Capture Graph Builder nasconde la finestra video chiamando [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il **valore OAFALSE**. Se in seguito l'applicazione chiama **RenderStream** con **PIN CATEGORY \_ \_ PREVIEW,** capture Graph Builder chiama insere **\_ AutoShow** con il valore **OATRUE** per visualizzare la finestra video.

Dopo aver chiamato **RenderStream** con **PIN CATEGORY \_ \_ CAPTURE,** è possibile verificare se è stato aggiunto il renderer video tramite una query in Filter Graph Manager per l'interfaccia [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



