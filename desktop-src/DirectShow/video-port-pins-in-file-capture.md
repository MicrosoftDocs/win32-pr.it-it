---
description: PIN della porta video nell'acquisizione di file
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: PIN della porta video nell'acquisizione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308955"
---
# <a name="video-port-pins-in-file-capture"></a>PIN della porta video nell'acquisizione di file

Se il dispositivo di acquisizione ha una porta video, il PIN della porta video deve essere connesso a un renderer video, anche se si vuole solo acquisire in un file.

Se si chiama [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con il valore **di \_ \_ acquisizione categoria pin** e il dispositivo ha un PIN della porta video, il generatore del grafico di acquisizione connette automaticamente il PIN della porta video al filtro [Overlay Mixer](overlay-mixer-filter.md) e connette il mixer sovrapposto al renderer video. Il generatore di grafici di acquisizione nasconde la finestra video chiamando [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con il valore **OAFALSE**. Se l'applicazione chiama in seguito **RenderStream** con la **\_ categoria pin \_ Preview**, il generatore del grafico di acquisizione chiama **put \_ AutoShow** con il valore **OATRUE** per visualizzare la finestra del video.

Dopo aver chiamato **RenderStream** con **l' \_ \_ acquisizione della categoria pin**, è possibile verificare se è stato aggiunto il renderer video eseguendo una query su Filter Graph Manager per l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



