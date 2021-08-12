---
title: Abilitazione delle notifiche
description: Abilitazione delle notifiche
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Gestione dispositivi multimediali, notifiche
- Gestione dispositivi, notifiche
- guida per programmatori,notifiche
- applicazioni desktop, notifiche
- creazione Windows applicazioni di Gestione dispositivi multimediali,notifiche
- Notifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ab1b71482db78571f141b7042d8abc926b0d79ca2f487ee7dc961396993b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585064"
---
# <a name="enabling-notifications"></a>Abilitazione delle notifiche

Windows Gestione dispositivi multimediali dichiara quattro interfacce che un'applicazione può implementare in una classe COM per ricevere notifiche degli eventi. Queste interfacce rientrano in due gruppi, come illustrato nella tabella seguente.



| Interfacce                                                                                                                                                | Descrizione                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Notifica all'applicazione quando i dispositivi o i supporti di archiviazione sono connessi o disconnessi.                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Un sistema di notifica molto semplice per avvisare un'applicazione dello stato di avanzamento di qualsiasi evento. L'applicazione non deve eseguire alcuna azione in risposta a questi messaggi. |



 

**IWMDMNotification**

**IWMDMNotification** avvisa l'applicazione quando i dispositivi Plug and Play sono connessi o disconnessi dal computer, nonché quando vengono inseriti o rimossi supporti di archiviazione Plug and Play (ad esempio schede flash). Queste notifiche consentono all'applicazione di aggiornare l'interfaccia utente per riflettere le modifiche.

Per ricevere queste notifiche, l'applicazione deve registrarsi per riceverle usando le interfacce **IConnectionPointContainer** e **IConnectionPoint** di Platform SDK. L'applicazione deve registrarsi per ricevere eventi all'avvio e annullare la registrazione alla chiusura. Seguire questa procedura per eseguire la registrazione per ricevere queste notifiche.

1.  Eseguire una query **sull'interfaccia IWMDeviceManager** principale ricevuta quando l'applicazione è stata autenticata per **IConnectionPointContainer.**
2.  Chiamare **IConnectionPointContainer::FindConnectionPoint** per recuperare un punto di connessione del contenitore per **le interfacce IWMDMNotification.**
3.  Registrarsi per ricevere eventi chiamando **IConnectionPoint::Advise**. Passare la classe che implementa **IWMDMNotification** e recuperare un cookie, un ID univoco che identifica il punto di connessione. Deve essere archiviato e usato in un secondo momento per annullare la registrazione per le notifiche degli eventi.

Il codice C++ seguente illustra come è possibile eseguire la registrazione per ricevere notifiche **da IWMDMNotification**.


```C++
HRESULT CWMDMController::RegisterForNotifications()
{
    HRESULT hr = S_OK;
    CComPtr<IConnectionPointContainer> pConxnPointCont;
    CComPtr<IConnectionPoint> pIConnPoint;

    // Get the IConnectionPointContainer interface from IWMDeviceManager.
    if (SUCCEEDED (hr = m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer, (void**) & pConxnPointCont)))
    {
        // Get a connection point from the container.
        if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
        {
            // Add ourselves as a callback handler for the connection point.
            // If we succeeded, indicate that by storing the connection point ID.
            DWORD dwCookie;
            if (SUCCEEDED (hr = pIConnPoint->Advise((IUnknown*)((IWMDMNotification*)this), &dwCookie)))
            {
                m_dwNotificationCookie = dwCookie;
            }
        }
    }

    return hr;
}
```



Quando l'applicazione viene chiusa, è necessario annullare la registrazione con **IConnectionPoint** per indicare che non deve più inviare notifiche. Seguire questa procedura per annullare la registrazione per le notifiche:

1.  Eseguire una query **sull'interfaccia IWMDeviceManager** principale per **IConnectionPointContainer.**
2.  Ottenere un punto di connessione **per le interfacce IWMDMNotification.**
3.  Annullare la registrazione dell'applicazione per le notifiche degli eventi chiamando **IConnectionPoint::Unadvise**, passando l'ID univoco ricevuto al momento della registrazione per ricevere gli eventi.

Il codice C++ seguente illustra come annullare la registrazione per gli **eventi IWMDMNotification** alla chiusura dell'applicazione.


```C++
HRESULT CWMDMController::UnregisterForNotifications()
{
    HRESULT hr = S_FALSE;

    // On class initialization, we initialized the handle to -1 as a flag 
    // to indicate we had not yet registered for notifications. If registration 
    // never happened, don't bother to unregister.
    if (-1 != m_dwNotificationCookie)
    {
        CComPtr<IConnectionPointContainer> pConxnPointCont;
        CComPtr<IConnectionPoint> pIConnPoint;

        // Get the connection point container from IWMDeviceManager. 
        if (SUCCEEDED (hr = 
           m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer,
           (void**) & pConxnPointCont)))
        {
            // Get a connection point from the container.
            if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
            {
                // Remove ourselves as a callback from the connection point.
                // If successful, reset the ID to a flag value.
                if (SUCCEEDED (hr = 
                    pIConnPoint->Unadvise(m_dwNotificationCookie)))
                {
                    m_dwNotificationCookie = -1;
                    hr = S_OK;
                }
            }
        }
    }

    return hr;
}
```



**Uso di IWMDMProgress**

Windows Gestione dispositivi multimediali può inviare messaggi di stato dell'applicazione quando si verificano azioni specifiche, ad esempio il trasferimento del contenuto, l'acquisizione dell'orologio sicuro e l'acquisizione di informazioni sui file DRM. L'applicazione può usare questi messaggi per monitorare lo stato dell'evento o annullare un evento. Per usare questa interfaccia, implementare [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)o [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)e passarla come parametro a un metodo che accetterà un messaggio di stato. Si noti **che IWMDMProgress3** è l'interfaccia superiore perché fornisce un GUID di identificazione che specifica quale azione viene rilevata. I metodi dell'applicazione seguenti accettano un'interfaccia di stato (i metodi del provider di servizi corrispondenti devono essere in grado di inviare notifiche a un'interfaccia inviata):

[**IWMDMStorageControl::D elete**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl::Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl::Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals::Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

Nella documentazione relativa a questi metodi vengono forniti esempi di passaggio di un'interfaccia in un metodo. Per esempi di implementazione delle interfacce di callback, vedere la documentazione relativa ai metodi **di IWMDMProgress**, **IWMDMProgress2** o **IWMDMProgress3**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'Windows di Gestione dispositivi multimediali**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





