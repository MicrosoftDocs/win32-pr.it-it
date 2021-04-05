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
# <a name="enabling-notifications"></a><span data-ttu-id="bd18c-109">Abilitazione di notifiche</span><span class="sxs-lookup"><span data-stu-id="bd18c-109">Enabling Notifications</span></span>

<span data-ttu-id="bd18c-110">Windows Media Gestione dispositivi dichiara quattro interfacce che un'applicazione può implementare in una classe COM per ricevere le notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="bd18c-110">Windows Media Device Manager declares four interfaces that an application can implement in a COM class to receive event notifications.</span></span> <span data-ttu-id="bd18c-111">Queste interfacce rientrano in due gruppi, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bd18c-111">These interfaces fall into two groups, as shown in the following table.</span></span>



| <span data-ttu-id="bd18c-112">Interfacce</span><span class="sxs-lookup"><span data-stu-id="bd18c-112">Interfaces</span></span>                                                                                                                                                | <span data-ttu-id="bd18c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd18c-113">Description</span></span>                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd18c-114">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="bd18c-114">**IWMDMNotification**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | <span data-ttu-id="bd18c-115">Notifica all'applicazione quando i dispositivi o i supporti di archiviazione sono connessi o disconnessi.</span><span class="sxs-lookup"><span data-stu-id="bd18c-115">Notifies the application when devices or storage media are connected or disconnected.</span></span>                                                                                         |
| [<span data-ttu-id="bd18c-116">**IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="bd18c-116">**IWMDMProgress**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [<span data-ttu-id="bd18c-117">**IWMDMProgress2**</span><span class="sxs-lookup"><span data-stu-id="bd18c-117">**IWMDMProgress2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [<span data-ttu-id="bd18c-118">**IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="bd18c-118">**IWMDMProgress3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | <span data-ttu-id="bd18c-119">Un sistema di notifica molto semplice per avvisare un'applicazione sullo stato di avanzamento di qualsiasi evento.</span><span class="sxs-lookup"><span data-stu-id="bd18c-119">A very simple notification system to alert an application about the progress of any event.</span></span> <span data-ttu-id="bd18c-120">Non è necessario che l'applicazione intraprenda azioni in risposta a questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="bd18c-120">The application is not required to take any actions in response to these messages.</span></span> |



 

<span data-ttu-id="bd18c-121">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="bd18c-121">**IWMDMNotification**</span></span>

<span data-ttu-id="bd18c-122">**IWMDMNotification** avvisa l'applicazione quando plug and Play dispositivi sono connessi o disconnessi dal computer, nonché quando plug and Play supporti di archiviazione (ad esempio, le schede flash) vengono inseriti o rimossi dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd18c-122">**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device.</span></span> <span data-ttu-id="bd18c-123">Queste notifiche possono consentire all'applicazione di aggiornare l'interfaccia utente in modo da riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="bd18c-123">These notifications can help the application update its user interface to reflect changes.</span></span>

<span data-ttu-id="bd18c-124">Per ricevere queste notifiche, l'applicazione deve registrarsi per riceverle usando le interfacce **IConnectionPointContainer** e **ICONNECTIONPOINT** di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="bd18c-124">In order to receive these notifications, your application must register to receive them using the Platform SDK **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="bd18c-125">L'applicazione deve registrarsi per ricevere eventi all'avvio e annullare la registrazione al momento della chiusura.</span><span class="sxs-lookup"><span data-stu-id="bd18c-125">Your application should register to receive events when it starts up, and unregister when it closes.</span></span> <span data-ttu-id="bd18c-126">Attenersi alla procedura seguente per effettuare la registrazione per ricevere queste notifiche.</span><span class="sxs-lookup"><span data-stu-id="bd18c-126">Follow these steps to register to receive these notifications.</span></span>

1.  <span data-ttu-id="bd18c-127">Eseguire una query sull'interfaccia **IWMDeviceManager** principale ricevuta quando è stata autenticata l'applicazione per **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="bd18c-127">Query the main **IWMDeviceManager** interface you received when you authenticated your application for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="bd18c-128">Chiamare **IConnectionPointContainer:: FindConnectionPoint** per recuperare un punto di connessione del contenitore per le interfacce **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="bd18c-128">Call **IConnectionPointContainer::FindConnectionPoint** to retrieve a container connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="bd18c-129">Eseguire la registrazione per ricevere eventi chiamando **IConnectionPoint:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="bd18c-129">Register to receive events by calling **IConnectionPoint::Advise**.</span></span> <span data-ttu-id="bd18c-130">Passare la classe che implementa **IWMDMNotification** e recuperare un cookie, un ID univoco che identifica il punto di connessione.</span><span class="sxs-lookup"><span data-stu-id="bd18c-130">Pass in the class that implements **IWMDMNotification**, and retrieve a cookie, a unique ID that identifies your connection point.</span></span> <span data-ttu-id="bd18c-131">Questo deve essere archiviato e usato in seguito per annullare la registrazione per le notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="bd18c-131">This must be stored, and used later to unregister for event notifications.</span></span>

<span data-ttu-id="bd18c-132">Nel codice C++ riportato di seguito viene illustrato come è possibile eseguire la registrazione per ricevere notifiche da **IWMDMNotification**.</span><span class="sxs-lookup"><span data-stu-id="bd18c-132">The following C++ code demonstrates how you can register to receive notifications from **IWMDMNotification**.</span></span>


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



<span data-ttu-id="bd18c-133">Quando l'applicazione viene chiusa, è necessario annullare la registrazione con **IConnectionPoint** per indicare che non deve più inviare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="bd18c-133">When your application closes, you must unregister with **IConnectionPoint** to indicate that it should no longer send you notifications.</span></span> <span data-ttu-id="bd18c-134">Per annullare la registrazione per le notifiche, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="bd18c-134">Follow these steps to unregister for notifications:</span></span>

1.  <span data-ttu-id="bd18c-135">Eseguire una query sull'interfaccia principale di **IWMDeviceManager** per **IConnectionPointContainer**.</span><span class="sxs-lookup"><span data-stu-id="bd18c-135">Query the main **IWMDeviceManager** interface for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="bd18c-136">Ottenere un punto di connessione per le interfacce **IWMDMNotification** .</span><span class="sxs-lookup"><span data-stu-id="bd18c-136">Get a connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="bd18c-137">Annullare la registrazione dell'applicazione per le notifiche degli eventi chiamando **IConnectionPoint:: Unadvise**, passando l'ID univoco ricevuto quando è stata eseguita la registrazione per la ricezione di eventi.</span><span class="sxs-lookup"><span data-stu-id="bd18c-137">Unregister your application for event notifications by calling **IConnectionPoint::Unadvise**, passing in the unique ID received when you registered to receive events.</span></span>

<span data-ttu-id="bd18c-138">Il codice C++ seguente mostra come annullare la registrazione degli eventi **IWMDMNotification** quando l'applicazione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="bd18c-138">The following C++ code shows how to unregister for **IWMDMNotification** events when your application closes.</span></span>


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



<span data-ttu-id="bd18c-139">**Uso di IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="bd18c-139">**Using IWMDMProgress**</span></span>

<span data-ttu-id="bd18c-140">Windows Media Gestione dispositivi può inviare i messaggi di stato dell'applicazione quando si verificano azioni specifiche, ad esempio il trasferimento di contenuto, l'acquisizione del clock sicuro e la presenza di informazioni sui file DRM.</span><span class="sxs-lookup"><span data-stu-id="bd18c-140">Windows Media Device Manager can send your application status messages when specific actions, such as content transfer, secure clock acquisition, and encountering DRM file information, occur.</span></span> <span data-ttu-id="bd18c-141">L'applicazione può usare questi messaggi per monitorare lo stato dell'evento o annullare un evento.</span><span class="sxs-lookup"><span data-stu-id="bd18c-141">Your application can use these messages to monitor the status of the event or cancel an event.</span></span> <span data-ttu-id="bd18c-142">Per usare questa interfaccia, implementare [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)o [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)e passarla come parametro a un metodo che accetterà un messaggio di stato.</span><span class="sxs-lookup"><span data-stu-id="bd18c-142">To use this interface, implement [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2), or [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), and pass it in as a parameter to a method that will accept a progress message.</span></span> <span data-ttu-id="bd18c-143">Si noti che **IWMDMProgress3** è l'interfaccia superiore perché fornisce un GUID di identificazione che specifica l'azione da rilevare.</span><span class="sxs-lookup"><span data-stu-id="bd18c-143">Note that **IWMDMProgress3** is the superior interface because it provides an identification GUID that specifies what action is being tracked.</span></span> <span data-ttu-id="bd18c-144">I metodi dell'applicazione seguenti accettano un'interfaccia di stato (i metodi del provider di servizi corrispondenti devono essere in grado di inviare notifiche a un'interfaccia inviata):</span><span class="sxs-lookup"><span data-stu-id="bd18c-144">The following application methods accept a progress interface (the corresponding service provider methods should be able to send notifications to a submitted interface):</span></span>

[<span data-ttu-id="bd18c-145">**IWMDMStorageControl::D Elimina**</span><span class="sxs-lookup"><span data-stu-id="bd18c-145">**IWMDMStorageControl::Delete**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[<span data-ttu-id="bd18c-146">**IWMDMStorageControl:: Insert**</span><span class="sxs-lookup"><span data-stu-id="bd18c-146">**IWMDMStorageControl::Insert**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[<span data-ttu-id="bd18c-147">**IWMDMStorageControl:: Move**</span><span class="sxs-lookup"><span data-stu-id="bd18c-147">**IWMDMStorageControl::Move**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[<span data-ttu-id="bd18c-148">**IWMDMStorageControl:: Read**</span><span class="sxs-lookup"><span data-stu-id="bd18c-148">**IWMDMStorageControl::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[<span data-ttu-id="bd18c-149">**IWMDMStorageControl:: Rename**</span><span class="sxs-lookup"><span data-stu-id="bd18c-149">**IWMDMStorageControl::Rename**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[<span data-ttu-id="bd18c-150">**IWMDMStorageControl2::Insert2**</span><span class="sxs-lookup"><span data-stu-id="bd18c-150">**IWMDMStorageControl2::Insert2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[<span data-ttu-id="bd18c-151">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="bd18c-151">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[<span data-ttu-id="bd18c-152">**IWMDMStorageGlobals:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="bd18c-152">**IWMDMStorageGlobals::Initialize**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[<span data-ttu-id="bd18c-153">**IWMDRMDeviceApp::AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="bd18c-153">**IWMDRMDeviceApp::AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)

<span data-ttu-id="bd18c-154">Esempi di passaggio di un'interfaccia in un metodo sono forniti nella documentazione per questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bd18c-154">Examples of passing an interface into a method are given in the documentation for these methods.</span></span> <span data-ttu-id="bd18c-155">Per esempi di implementazione delle interfacce di callback, vedere la documentazione relativa ai metodi di **IWMDMProgress**, **IWMDMProgress2** o **IWMDMProgress3**.</span><span class="sxs-lookup"><span data-stu-id="bd18c-155">For examples of implementing the callback interfaces, see the documentation for the methods of **IWMDMProgress**, **IWMDMProgress2**, or **IWMDMProgress3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd18c-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd18c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd18c-157">**Creazione di un'applicazione Windows Media Gestione dispositivi**</span><span class="sxs-lookup"><span data-stu-id="bd18c-157">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





