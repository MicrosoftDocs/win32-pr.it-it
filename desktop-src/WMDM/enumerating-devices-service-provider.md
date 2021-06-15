---
title: Enumerazione dei dispositivi (WMDM)
description: Gestione dispositivi Windows Media gestisce una cache di dispositivi connessi. Informazioni su come Gestione dispositivi Windows Media gestisce o aggiorna la cache.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Gestione dispositivi Windows Media, enumerazione dei dispositivi
- Gestione dispositivi, enumerazione dei dispositivi
- guida per programmatori, enumerazione di dispositivi
- provider di servizi, enumerazione di dispositivi
- creazione di provider di servizi, enumerazione dei dispositivi
- enumerazione di dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067908"
---
# <a name="enumerating-devices-wmdm"></a>Enumerazione dei dispositivi (WMDM)

Gestione dispositivi Windows Media gestisce una cache di dispositivi connessi che viene aggiornata all'avvio di un'applicazione Gestione dispositivi Windows Media, quando un dispositivo Plug and Play (PnP) si connette o si disconnette o quando l'applicazione chiama [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Questa cache viene esposta all'applicazione quando chiama [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Ogni dispositivo viene esposto all'applicazione come [**interfaccia IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) Se il provider di servizi è registrato per gestire i dispositivi PnP, Gestione dispositivi Windows Media sarà a conoscenza dell'elenco corrente dei dispositivi connessi. Se il provider di servizi è registrato per gestire dispositivi non PnP, il provider di servizi è responsabile dell'individuazione dei dispositivi collegati. Un provider di servizi può essere registrato solo per dispositivi PnP o non PnP, mai entrambi.

Le azioni seguenti mostrano come Gestione dispositivi Windows Media gestisce o aggiorna la cache. Si noti che la cache non viene mai aggiornata quando un dispositivo non PnP si connette o si disconnette.

Viene avviata un'applicazione Gestione dispositivi Windows Media

-   Gestione dispositivi Windows Media recupera un elenco di dispositivi PnP collegati dal sottosistema PnP e chiama [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) nel sp registrato per ogni dispositivo connesso. Individua il provider di servizi corretto tramite una query sul parametro del dispositivo WMDMSPCLSID per l'ID classe del provider di servizi responsabile del dispositivo. Per [altre informazioni, vedere](device-parameters.md) Parametri del dispositivo. Tutti i dispositivi restituiti vengono aggiunti alla cache dei dispositivi di Gestione dispositivi Windows Media.
-   Gestione dispositivi Windows Media trova tutti i provider di servizi non PnP registrati con esso e chiama [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) in ogni provider di servizi per ottenere un elenco di dispositivi da ognuno. Tutti i dispositivi restituiti vengono aggiunti alla cache.

L'applicazione chiama IWMDeviceManager/2::EnumDevices/2

-   Gestione dispositivi Windows Media restituisce il relativo elenco di dispositivi memorizzati nella cache.

Un dispositivo PnP si connette

-   Gestione dispositivi Windows Media trova il provider di servizi pertinente e chiama **IMDServiceProvider2::CreateDevice** e aggiunge il dispositivo alla cache.
-   Se l'applicazione implementa [**IWMDMNotification,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)Gestione dispositivi Windows Media chiama [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) con una notifica di arrivo.

Un dispositivo PnP si disconnette

-   Gestione dispositivi Windows Media rimuove l'elemento dalla cache.
-   Se l'applicazione implementa IWMDMNotification, Gestione dispositivi Windows Media chiama IWMDMNotification::WMDMMessage con una notifica di partenza.

L'applicazione chiama IWMDeviceManager2::Reinitialize

-   Aggiorna la cache con tutti i dispositivi connessi.

Un dispositivo non PnP si connette o si disconnette

-   Gestione dispositivi Windows Media non è informato dell'arrivo o della partenza e non prende alcuna azione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




