---
description: Dopo aver iniziato l'anteprima di un flusso video, chiamare il metodo IWiaVideo::TakePicture dell'interfaccia IWiaVideo per acquisire un'immagine fissa dal video in streaming.
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Acquisizione di un'immagine ancorata da un flusso video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af98dc313ddde7f2da160515ab53d31357a6d9cc96e1737ed01767b40fb0e7c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814281"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Acquisizione di un'immagine ancorata da un flusso video

Dopo aver iniziato l'anteprima di un flusso video, chiamare il metodo [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) [**dell'interfaccia IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) per acquisire un'immagine fissa dal video in streaming. Per istruzioni su come ottenere un **puntatore IWiaVideo** e iniziare a visualizzare in anteprima i video in streaming, vedere [Anteprima dei video.](-wia-previewing-video.md)

Quando viene restituito il metodo [**IWiaVideo::TakePicture,**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) il parametro *pbstrNewImageFilename* contiene il percorso completo e il nome file del file di immagine risultante. Il file è in formato JPEG. La directory in cui viene creato il file viene specificata dal valore della proprietà [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) [**dell'interfaccia IWiaVideo.**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)

> [!Note]  
> Windows Acquisizione di immagini (WIA) non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive. Per queste versioni del Windows, [usare](/previous-versions//ms783323(v=vs.85)) DirectShow per acquisire immagini dal video.

 

 

 
