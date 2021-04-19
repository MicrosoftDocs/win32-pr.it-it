---
description: Viene illustrato come utilizzare Wi-Fi funzioni dirette nelle applicazioni desktop.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Uso delle funzioni Wi-Fi dirette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311659"
---
# <a name="using-the-wi-fi-direct-functions"></a><span data-ttu-id="3f7ba-103">Uso delle funzioni Wi-Fi dirette</span><span class="sxs-lookup"><span data-stu-id="3f7ba-103">Using the Wi-Fi Direct functions</span></span>

<span data-ttu-id="3f7ba-104">In questo argomento viene illustrato come utilizzare Wi-Fi funzioni dirette nelle applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-104">This topics shows how to use Wi-Fi Direct functions in desktop apps.</span></span> <span data-ttu-id="3f7ba-105">A partire da Windows 8 e Windows Server 2012, Wi-Fi funzioni dirette sono state aggiunte all'API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="3f7ba-106">La funzionalità Wi-Fi diretta è basata sullo sviluppo della Wi-Fi specifiche tecniche peer-to-Peer v 1.1 da Wi-Fi Alliance (vedere le [specifiche pubblicate in Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="3f7ba-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="3f7ba-107">L'obiettivo della specifica tecnica peer-to-peer Wi-Fi è fornire una soluzione per Wi-Fi la connettività da dispositivo a dispositivo senza che sia necessario un punto di accesso wireless (AP wireless) per configurare la connessione o l'utilizzo del meccanismo di Wi-Fi ad hoc (IBSS) esistente.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="3f7ba-108">La modalità ad hoc potrebbe non essere disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="3f7ba-109">A partire da Windows 8.1 e Windows Server 2012 R2, usare invece Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="3f7ba-110">Le funzioni seguenti supportano la funzionalità Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-110">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="3f7ba-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indica che l'app vuole annullare una funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) in sospeso che non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="3f7ba-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : chiude un handle per il servizio diretto Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="3f7ba-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : chiude una sessione dopo una chiamata precedentemente riuscita alla funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="3f7ba-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="3f7ba-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : apre un handle per il servizio Wi-Fi Direct e negozia una versione dell'API Wi-Fi Direct da usare.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="3f7ba-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : recupera e applica un profilo archiviato per un dispositivo Wi-Fi Direct legacy.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="3f7ba-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : avvia una connessione su richiesta a un dispositivo Wi-Fi diretto specifico, che è stato precedentemente abbinato tramite l'esperienza di abbinamento di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="3f7ba-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : aggiorna la visibilità del dispositivo per l'indirizzo Wi-Fi diretto del dispositivo per un determinato nodo del dispositivo Wi-Fi diretto installato.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="3f7ba-118">[**Direttiva \_ di Apri \_ \_ \_ callback completo della sessione**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : definisce la funzione di callback chiamata dalla funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) al completamento dell'operazione **WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-118">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="3f7ba-119">Per un'app desktop, la funzionalità Wi-Fi Direct richiede che i dispositivi Wi-FI Direct siano in precedenza abbinati dall'utente con l'interfaccia utente di Windows pairing Experience.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-119">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="3f7ba-120">Una volta completata questa associazione, viene archiviato un profilo che consente di usare le funzioni dirette di Wi-Fi per avviare una sessione di Wi-Fi Direct per stabilire una connessione tra il Wi-Fi i dispositivi diretti.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-120">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="3f7ba-121">Per usare Wi-Fi Direct, un'app deve prima ottenere un handle per il servizio Wi-Fi Direct chiamando la funzione [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) .</span><span class="sxs-lookup"><span data-stu-id="3f7ba-121">In order to use Wi-Fi Direct, an app must first obtain a handle to the Wi-Fi Direct service by calling the [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) function.</span></span> <span data-ttu-id="3f7ba-122">Il Wi-Fi handle diretto (GMA) restituito dalla funzione **WFDOpenHandle** viene usato per le successive chiamate di funzione Wi-Fi dirette effettuate al servizio Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-122">The Wi-Fi Direct (WFD) handle returned by the **WFDOpenHandle** function is used for subsequent Wi-Fi Direct function calls made to the Wi-Fi Direct service.</span></span>

<span data-ttu-id="3f7ba-123">La funzione [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) avvia un'operazione asincrona per avviare una connessione su richiesta a una specifica Wi-Fi dispositivo diretto.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-123">The [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function starts an asynchronous operation to start an on-demand connection to a specific Wi-Fi Direct device.</span></span> <span data-ttu-id="3f7ba-124">Il dispositivo Wi-Fi di destinazione deve essere stato abbinato in precedenza tramite l'esperienza di associazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-124">The target Wi-Fi device must previously have been paired through the Windows Pairing experience.</span></span> <span data-ttu-id="3f7ba-125">Quando l'operazione asincrona viene completata, viene chiamata la funzione di callback specificata nel parametro *pfnCallback* .</span><span class="sxs-lookup"><span data-stu-id="3f7ba-125">When the asynchronous operation completes, the callback function specified in the *pfnCallback* parameter is called.</span></span>

<span data-ttu-id="3f7ba-126">Quando un'applicazione viene eseguita utilizzando il servizio Wi-Fi Direct, l'applicazione deve chiamare la funzione [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) per segnalare al servizio Wi-Fi diretto che l'applicazione viene eseguita utilizzando il servizio.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-126">Once an application is done using the Wi-Fi Direct service, the application should call the [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) function to signal to the Wi-Fi Direct service that the application is done using the service.</span></span> <span data-ttu-id="3f7ba-127">Questo consente all'Wi-Fi servizio diretto di rilasciare le risorse usate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f7ba-127">This allows the Wi-Fi Direct service to release resources used by the application.</span></span>

<span data-ttu-id="3f7ba-128">Per altre informazioni su Wi-Fi Direct per l'uso nelle app di Windows Store, vedere [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e le classi correlate nello spazio dei nomi [**Windows. Networking. prossimità**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="3f7ba-128">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f7ba-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f7ba-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3f7ba-130">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-130">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3f7ba-131">Informazioni sul Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="3f7ba-131">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="3f7ba-132">Informazioni sull'API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="3f7ba-132">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="3f7ba-133">Informazioni sulla funzionalità Wi-Fi Direct</span><span class="sxs-lookup"><span data-stu-id="3f7ba-133">About the Wi-Fi Direct feature</span></span>](about-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="3f7ba-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3f7ba-135">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-135">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="3f7ba-136">**\_ \_ callback completo della sessione di apertura della \_ direttiva GMA \_**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-136">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="3f7ba-137">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-137">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="3f7ba-138">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-138">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="3f7ba-139">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-139">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="3f7ba-140">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-140">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="3f7ba-141">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-141">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="3f7ba-142">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-142">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="3f7ba-143">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-143">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="3f7ba-144">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="3f7ba-144">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
