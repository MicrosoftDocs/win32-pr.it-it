---
description: L'interfaccia IWiaVideo consente a un'applicazione di visualizzare video e acquisire immagini fisse da essa.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Anteprima di video (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca270adf4e6461beac409315c782101744e8afeb72c33f07aa7bbc999e24751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813721"
---
# <a name="previewing-video-wia"></a>Anteprima di video (WIA)

[**L'interfaccia IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) consente a un'applicazione di visualizzare video e acquisire immagini fisse da essa. Seguire questa procedura per selezionare il dispositivo video in streaming e visualizzare un flusso video in una finestra.

-   Chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un puntatore [**all'interfaccia IWiaDevMgr.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)
-   Usare il [**metodo IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) dell'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) per ottenere un [**puntatore all'interfaccia IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) Per istruzioni su come enumerare i dispositivi, vedere Enumerazione dei dispositivi di sistema.
-   Usare [**l'interfaccia IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) per ottenere un puntatore a interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ogni dispositivo WIA (Windows Image Acquisition) trovato.
-   Usare [**l'interfaccia IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ottenere la proprietà DeviceID del dispositivo desiderato. Un dispositivo video in streaming ha il flag StiDeviceTypeStreamingVideo della proprietà WIA \_ DIP \_ DEV TYPE \_ impostata.
-   Usare [**l'interfaccia IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ottenere il valore della proprietà \_ DIRECTORY WIA DPV \_ \_ IMAGES.
-   Chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un puntatore [**all'interfaccia IWiaVideo.**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)
-   Impostare la [**proprietà IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) dell'interfaccia [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) sul valore ricevuto dal valore della proprietà DIRECTORY WIA \_ DPV \_ \_ IMAGES.
-   Chiamare [**IWiaVideo::CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) [**sull'interfaccia IWiaVideo,**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) passando l'ID dispositivo del dispositivo dell'immagine di streaming e l'handle della finestra in cui deve essere visualizzato il video.

> [!Note]  
> WIA non supporta i dispositivi video in Windows Server 2003, Windows Vista o versioni successive. Per queste versioni del Windows, [usare](/previous-versions//ms783323(v=vs.85)) DirectShow per acquisire immagini dal video.

 

 

 
