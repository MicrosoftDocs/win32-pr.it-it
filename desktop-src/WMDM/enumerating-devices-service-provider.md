---
title: Enumerazione dei dispositivi (WMDM)
description: Windows Gestione dispositivi multimediali mantiene una cache dei dispositivi connessi. Informazioni su Windows Gestione dispositivi multimediali gestisce o aggiorna la cache.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Gestione dispositivi multimediali, enumerazione dei dispositivi
- Gestione dispositivi, enumerazione dei dispositivi
- guida alla programmazione, enumerazione di dispositivi
- provider di servizi, enumerazione di dispositivi
- creazione di provider di servizi, enumerazione di dispositivi
- enumerazione di dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500375f01e718ab6f9824868ffabd7c83e11c3e812ce0288f0c15186bc1d2de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767051"
---
# <a name="enumerating-devices-wmdm"></a>Enumerazione dei dispositivi (WMDM)

Windows Gestione dispositivi multimediali mantiene una cache dei dispositivi connessi che viene aggiornata all'avvio di un'applicazione di Gestione dispositivi multimediali di Windows, quando un dispositivo Plug and Play (PnP) si connette o si disconnette o quando l'applicazione chiama [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Questa cache viene esposta all'applicazione quando chiama [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) o [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Ogni dispositivo viene esposto all'applicazione come [**interfaccia IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) Se il provider di servizi è registrato per gestire i dispositivi PnP, Windows Gestione dispositivi multimediali sarà a conoscenza dell'elenco corrente dei dispositivi connessi. Se il provider di servizi è registrato per gestire i dispositivi non PnP, il provider di servizi è responsabile dell'individuazione dei dispositivi collegati. Un provider di servizi può essere registrato solo per dispositivi PnP o non PnP, mai entrambi.

Le azioni seguenti mostrano come Windows Gestione dispositivi multimediali gestisce o aggiorna la cache. Si noti che la cache non viene mai aggiornata quando un dispositivo non PnP si connette o si disconnette.

Viene avviata Windows'applicazione Gestione dispositivi multimediali

-   Windows Gestione dispositivi multimediali recupera un elenco di dispositivi PnP collegati dal sottosistema PnP e chiama [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) nel provider di servizi registrato per ogni dispositivo connesso. Individua il provider di servizi corretto tramite una query sul parametro del dispositivo WMDMSPCLSID per l'ID di classe del provider di servizi responsabile del dispositivo. Per [altre informazioni, vedere](device-parameters.md) Parametri del dispositivo. Tutti i dispositivi restituiti vengono aggiunti alla cache Windows gestione dispositivi multimediali dei dispositivi.
-   Windows Gestione dispositivi multimediali trova tutti i provider di servizi non PnP registrati e chiama [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) in ogni provider di servizi per ottenere un elenco dei dispositivi da ognuno. Tutti i dispositivi restituiti vengono aggiunti alla cache.

L'applicazione chiama IWMDeviceManager/2::EnumDevices/2

-   Windows Gestione dispositivi multimediali restituisce il relativo elenco di dispositivi memorizzati nella cache.

Un dispositivo PnP si connette

-   Windows Gestione dispositivi multimediali trova il provider di servizi pertinente e chiama **IMDServiceProvider2::CreateDevice** e aggiunge il dispositivo alla cache.
-   Se l'applicazione implementa [**IWMDMNotification,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)Windows Gestione dispositivi multimediali chiama [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) con una notifica di arrivo.

Un dispositivo PnP si disconnette

-   Windows Gestione dispositivi multimediali rimuove l'elemento dalla cache.
-   Se l'applicazione implementa IWMDMNotification, Windows Gestione dispositivi multimediali chiama IWMDMNotification::WMDMMessage con una notifica di partenza.

L'applicazione chiama IWMDeviceManager2::Reinitialize

-   Aggiorna la cache con tutti i dispositivi connessi.

Un dispositivo non PnP si connette o si disconnette

-   Windows Gestione dispositivi multimediali non viene informato dell'arrivo o della partenza e non viene eseguita alcuna azione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




