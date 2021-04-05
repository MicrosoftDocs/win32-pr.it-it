---
title: Abilitazione di notifiche
description: Abilitazione di notifiche
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Media Gestione dispositivi, notifiche
- Gestione dispositivi, notifiche
- Guida per programmatori, notifiche
- applicazioni desktop, notifiche
- creazione di applicazioni Windows Media Gestione dispositivi, notifiche
- Notifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618356c9d63d20a8b6b14e6c99072074cfc75073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709697"
---
# <a name="enabling-notifications"></a>Abilitazione di notifiche

Windows Media Gestione dispositivi dichiara quattro interfacce che un'applicazione può implementare in una classe COM per ricevere le notifiche degli eventi. Queste interfacce rientrano in due gruppi, come illustrato nella tabella seguente.



| Interfacce                                                                                                                                                | Descrizione                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | Notifica all'applicazione quando i dispositivi o i supporti di archiviazione sono connessi o disconnessi.                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | Un sistema di notifica molto semplice per avvisare un'applicazione sullo stato di avanzamento di qualsiasi evento. Non è necessario che l'applicazione intraprenda azioni in risposta a questi messaggi. |



 

**IWMDMNotification**

**IWMDMNotification** avvisa l'applicazione quando plug and Play dispositivi sono connessi o disconnessi dal computer, nonché quando plug and Play supporti di archiviazione (ad esempio, le schede flash) vengono inseriti o rimossi dal dispositivo. Queste notifiche possono consentire all'applicazione di aggiornare l'interfaccia utente in modo da riflettere le modifiche.

Per ricevere queste notifiche, l'applicazione deve registrarsi per riceverle usando le interfacce **IConnectionPointContainer** e **ICONNECTIONPOINT** di Platform SDK. L'applicazione deve registrarsi per ricevere eventi all'avvio e annullare la registrazione al momento della chiusura. Attenersi alla procedura seguente per effettuare la registrazione per ricevere queste notifiche.

1.  Eseguire una query sull'interfaccia **IWMDeviceManager** principale ricevuta quando è stata autenticata l'applicazione per **IConnectionPointContainer**.
2.  Chiamare **IConnectionPointContainer:: FindConnectionPoint** per recuperare un punto di connessione del contenitore per le interfacce **IWMDMNotification** .
3.  Eseguire la registrazione per ricevere eventi chiamando **IConnectionPoint:: Advise**. Passare la classe che implementa **IWMDMNotification** e recuperare un cookie, un ID univoco che identifica il punto di connessione. Questo deve essere archiviato e usato in seguito per annullare la registrazione per le notifiche degli eventi.

Nel codice C++ riportato di seguito viene illustrato come è possibile eseguire la registrazione per ricevere notifiche da **IWMDMNotification**.


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



Quando l'applicazione viene chiusa, è necessario annullare la registrazione con **IConnectionPoint** per indicare che non deve più inviare le notifiche. Per annullare la registrazione per le notifiche, attenersi alla procedura seguente:

1.  Eseguire una query sull'interfaccia principale di **IWMDeviceManager** per **IConnectionPointContainer**.
2.  Ottenere un punto di connessione per le interfacce **IWMDMNotification** .
3.  Annullare la registrazione dell'applicazione per le notifiche degli eventi chiamando **IConnectionPoint:: Unadvise**, passando l'ID univoco ricevuto quando è stata eseguita la registrazione per la ricezione di eventi.

Il codice C++ seguente mostra come annullare la registrazione degli eventi **IWMDMNotification** quando l'applicazione viene chiusa.


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

Windows Media Gestione dispositivi può inviare i messaggi di stato dell'applicazione quando si verificano azioni specifiche, ad esempio il trasferimento di contenuto, l'acquisizione del clock sicuro e la presenza di informazioni sui file DRM. L'applicazione può usare questi messaggi per monitorare lo stato dell'evento o annullare un evento. Per usare questa interfaccia, implementare [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)o [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)e passarla come parametro a un metodo che accetterà un messaggio di stato. Si noti che **IWMDMProgress3** è l'interfaccia superiore perché fornisce un GUID di identificazione che specifica l'azione da rilevare. I metodi dell'applicazione seguenti accettano un'interfaccia di stato (i metodi del provider di servizi corrispondenti devono essere in grado di inviare notifiche a un'interfaccia inviata):

[**IWMDMStorageControl::D Elimina**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl:: Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl:: Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals:: Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

Esempi di passaggio di un'interfaccia in un metodo sono forniti nella documentazione per questi metodi. Per esempi di implementazione delle interfacce di callback, vedere la documentazione relativa ai metodi di **IWMDMProgress**, **IWMDMProgress2** o **IWMDMProgress3**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





