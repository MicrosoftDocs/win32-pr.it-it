---
description: L'interfaccia IWiaVideo consente a un'applicazione di visualizzare video e acquisire immagini ancora.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Anteprima del video (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935625c1c16ceea66326963185dd75d96d98ed02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526430"
---
# <a name="previewing-video-wia"></a>Anteprima del video (WIA)

L'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) consente a un'applicazione di visualizzare video e acquisire immagini ancora. Eseguire la procedura seguente per selezionare il dispositivo di streaming video e visualizzare un flusso video in una finestra.

-   Chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un puntatore all'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) .
-   Usare il metodo [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) dell'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) per ottenere un puntatore all'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Per istruzioni su come enumerare i dispositivi, vedere Enumerazione dei dispositivi di sistema.
-   Usare l'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) per ottenere un puntatore a interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ogni dispositivo Windows Image Acquisition (WIA) trovato.
-   Usare l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ottenere la proprietà DeviceID del dispositivo desiderato. Un dispositivo di streaming video ha il flag StiDeviceTypeStreamingVideo del \_ set di proprietà del tipo del dip di \_ sviluppo WIA \_ .
-   Usare l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ottenere il \_ valore della proprietà della directory WIA DPV \_ images \_ .
-   Chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un puntatore all'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .
-   Impostare la proprietà [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) dell'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) sul valore ricevuto dal valore della proprietà della \_ directory WIA DPV \_ images \_ .
-   Chiamare [**IWiaVideo:: CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) sull'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , passando l'ID dispositivo del dispositivo immagine di streaming e l'handle della finestra in cui deve essere visualizzato il video.

> [!Note]  
> WIA non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive. Per queste versioni di Windows, usare [DirectShow](/previous-versions//ms783323(v=vs.85)) per acquisire immagini dal video.

 

 

 
