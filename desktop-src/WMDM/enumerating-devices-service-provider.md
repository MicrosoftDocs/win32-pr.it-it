---
title: Enumerazione dei dispositivi (WMDM)
description: Enumerazione dei dispositivi
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Gestione dispositivi, enumerazione dei dispositivi
- Gestione dispositivi, enumerazione dei dispositivi
- Guida per programmatori, enumerazione dei dispositivi
- provider di servizi, enumerazione dei dispositivi
- creazione di provider di servizi, enumerazione dei dispositivi
- Enumerazione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316b87f6ad3f5680e0c22da832da7b1efec24629
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719552"
---
# <a name="enumerating-devices-wmdm"></a>Enumerazione dei dispositivi (WMDM)

Windows Media Gestione dispositivi gestisce una cache di dispositivi connessi che viene aggiornata all'avvio di un'applicazione Windows Media Gestione dispositivi, quando un dispositivo Plug and Play (PnP) si connette o si disconnette o quando l'applicazione chiama [**IWMDeviceManager2:: Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Questa cache viene esposta all'applicazione quando chiama [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Ogni dispositivo viene esposto all'applicazione come un'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) . Se il provider di servizi è registrato per gestire i dispositivi PnP, Windows Media Gestione dispositivi riconoscerà l'elenco corrente dei dispositivi connessi. Se il provider di servizi è registrato per gestire dispositivi non PnP, il provider di servizi è responsabile dell'individuazione dei dispositivi collegati. Un provider di servizi può essere registrato solo per dispositivi PnP o non PnP, mai entrambi.

Le azioni seguenti illustrano come Windows Media Gestione dispositivi gestisce o aggiorna la cache. Si noti che la cache non viene mai aggiornata quando un dispositivo non PnP si connette o si disconnette.

Viene avviata un'applicazione Windows Media Gestione dispositivi

-   Windows Media Gestione dispositivi recupera un elenco di dispositivi PnP collegati dal sottosistema PnP e chiama [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) sul SP registrato per ogni dispositivo connesso. (Individua il provider di servizi corretto eseguendo una query sul parametro di dispositivo WMDMSPCLSID per l'ID di classe del provider di servizi responsabile del dispositivo. Per ulteriori informazioni, vedere [parametri del dispositivo](device-parameters.md) . Tutti i dispositivi restituiti vengono aggiunti alla cache Windows Media Gestione dispositivi dei dispositivi.
-   Windows Media Gestione dispositivi trova tutti i provider di servizi non PnP registrati e chiama [**IMDServiceProvider:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) in ogni provider di servizi per ottenere un elenco di dispositivi da ognuno di essi. Tutti i dispositivi restituiti vengono aggiunti alla cache.

L'applicazione chiama IWMDeviceManager/2:: EnumDevices/2

-   Windows Media Gestione dispositivi restituisce l'elenco dei dispositivi memorizzati nella cache.

Connessione di un dispositivo PnP

-   Windows Media Gestione dispositivi trova il provider di servizi pertinente e chiama **IMDServiceProvider2:: CreateDevice** e aggiunge il dispositivo alla relativa cache.
-   Se l'applicazione implementa [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Gestione dispositivi chiama [**IWMDMNotification:: WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) con una notifica di arrivo.

Un dispositivo PnP si disconnette

-   Windows Media Gestione dispositivi rimuove l'elemento dalla relativa cache.
-   Se l'applicazione implementa IWMDMNotification, Windows Media Gestione dispositivi chiama IWMDMNotification:: WMDMMessage con una notifica di partenza.

L'applicazione chiama IWMDeviceManager2:: Reinitialize

-   Aggiorna la cache con tutti i dispositivi connessi.

Un dispositivo non PnP si connette o si disconnette

-   Windows Media Gestione dispositivi non viene informato dell'arrivo o della partenza e non esegue alcuna azione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




