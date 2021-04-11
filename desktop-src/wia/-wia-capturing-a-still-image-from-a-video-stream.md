---
description: "Dopo l'inizio dell'anteprima di un flusso video, chiamare il metodo IWiaVideo:: TakePicture dell'interfaccia IWiaVideo per acquisire un'immagine ancora dal video di streaming."
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Acquisizione di un'immagine ancora da un flusso video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be475405f4aa9719514a531a6af0105d7a786f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231560"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Acquisizione di un'immagine ancora da un flusso video

Dopo l'inizio dell'anteprima di un flusso video, chiamare il metodo [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) dell'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) per acquisire un'immagine ancora dal video di streaming. Per istruzioni su come ottenere un puntatore **IWiaVideo** e iniziare l'anteprima del video di streaming, vedere [anteprima del video](-wia-previewing-video.md).

Quando il metodo [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) restituisce, il parametro *pbstrNewImageFilename* contiene il percorso completo e il nome file del file di immagine risultante. Il file è in formato JPEG. La directory in cui viene creato il file è specificata dal valore della proprietà [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) dell'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .

> [!Note]  
> Windows Image Acquisition (WIA) non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive. Per queste versioni di Windows, usare [DirectShow](/previous-versions//ms783323(v=vs.85)) per acquisire immagini dal video.

 

 

 
