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
# <a name="capturing-a-still-image-from-a-video-stream"></a><span data-ttu-id="108fe-103">Acquisizione di un'immagine ancora da un flusso video</span><span class="sxs-lookup"><span data-stu-id="108fe-103">Capturing a Still Image from a Video Stream</span></span>

<span data-ttu-id="108fe-104">Dopo l'inizio dell'anteprima di un flusso video, chiamare il metodo [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) dell'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) per acquisire un'immagine ancora dal video di streaming.</span><span class="sxs-lookup"><span data-stu-id="108fe-104">After beginning preview of a video stream, call the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to capture a still image from the streaming video.</span></span> <span data-ttu-id="108fe-105">Per istruzioni su come ottenere un puntatore **IWiaVideo** e iniziare l'anteprima del video di streaming, vedere [anteprima del video](-wia-previewing-video.md).</span><span class="sxs-lookup"><span data-stu-id="108fe-105">For instructions on how to get an **IWiaVideo** pointer and begin previewing streaming video, see [Previewing Video](-wia-previewing-video.md).</span></span>

<span data-ttu-id="108fe-106">Quando il metodo [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) restituisce, il parametro *pbstrNewImageFilename* contiene il percorso completo e il nome file del file di immagine risultante.</span><span class="sxs-lookup"><span data-stu-id="108fe-106">When the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method returns, the *pbstrNewImageFilename* parameter contains the full path and filename of the resulting image file.</span></span> <span data-ttu-id="108fe-107">Il file è in formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="108fe-107">The file is in JPEG format.</span></span> <span data-ttu-id="108fe-108">La directory in cui viene creato il file è specificata dal valore della proprietà [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) dell'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .</span><span class="sxs-lookup"><span data-stu-id="108fe-108">The directory in which the file is created is specified by the value of the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>

> [!Note]  
> <span data-ttu-id="108fe-109">Windows Image Acquisition (WIA) non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="108fe-109">Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="108fe-110">Per queste versioni di Windows, usare [DirectShow](/previous-versions//ms783323(v=vs.85)) per acquisire immagini dal video.</span><span class="sxs-lookup"><span data-stu-id="108fe-110">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
