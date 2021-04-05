---
title: Interfaccia IRemoteDesktopClientEvents
description: Fornisce metodi che ricevono informazioni dal server correlate agli eventi di controllo client.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048367"
---
# <a name="iremotedesktopclientevents-interface"></a><span data-ttu-id="e39a7-105">Interfaccia IRemoteDesktopClientEvents</span><span class="sxs-lookup"><span data-stu-id="e39a7-105">IRemoteDesktopClientEvents interface</span></span>

<span data-ttu-id="e39a7-106">Fornisce metodi che ricevono informazioni dal server correlate agli eventi di controllo client.</span><span class="sxs-lookup"><span data-stu-id="e39a7-106">Provides methods that receive information from the server that are related to client control events.</span></span> <span data-ttu-id="e39a7-107">Gli eventi includono la connessione e la disconnessione, le richieste in modalità schermo intero, l'accesso riuscito e le condizioni di errore.</span><span class="sxs-lookup"><span data-stu-id="e39a7-107">Events include connecting and disconnecting, full-screen mode requests, successful logon, and error conditions.</span></span>

## <a name="members"></a><span data-ttu-id="e39a7-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e39a7-108">Members</span></span>

<span data-ttu-id="e39a7-109">L'interfaccia **IRemoteDesktopClientEvents** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e39a7-109">The **IRemoteDesktopClientEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e39a7-110">**IRemoteDesktopClientEvents** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e39a7-110">**IRemoteDesktopClientEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="e39a7-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e39a7-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e39a7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="e39a7-112">Methods</span></span>

<span data-ttu-id="e39a7-113">L'interfaccia **IRemoteDesktopClientEvents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e39a7-113">The **IRemoteDesktopClientEvents** interface has these methods.</span></span>



| <span data-ttu-id="e39a7-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="e39a7-114">Method</span></span>                                                                                      | <span data-ttu-id="e39a7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e39a7-115">Description</span></span>                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e39a7-116">**OnAdminMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="e39a7-116">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="e39a7-117">Chiamato quando il controllo client riceve un messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="e39a7-117">Called when the client control receives an administrative message.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="e39a7-118">**OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="e39a7-118">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="e39a7-119">Chiamato quando il controllo client si è riconnesso automaticamente a una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e39a7-119">Called when the client control has automatically reconnected to a remote session.</span></span> <br/>                                                                       |
| [<span data-ttu-id="e39a7-120">**OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="e39a7-120">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="e39a7-121">Chiamato quando il controllo client tenta di ristabilire automaticamente una connessione a una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e39a7-121">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span> <br/>                                                  |
| [<span data-ttu-id="e39a7-122">**OnConnected**</span><span class="sxs-lookup"><span data-stu-id="e39a7-122">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="e39a7-123">Chiamato quando il controllo client si è connesso a una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e39a7-123">Called when the client control has connected to a remote session.</span></span><br/>                                                                                        |
| [<span data-ttu-id="e39a7-124">**Onconnecting**</span><span class="sxs-lookup"><span data-stu-id="e39a7-124">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="e39a7-125">Chiamato quando il controllo client tenta di stabilire una connessione a una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e39a7-125">Called when the client control attempts to establish a connection to a remote session.</span></span> <br/>                                                                  |
| [<span data-ttu-id="e39a7-126">**OnDialogDismissed**</span><span class="sxs-lookup"><span data-stu-id="e39a7-126">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="e39a7-127">Chiamato dopo che una finestra di dialogo visualizzata dal controllo client viene rilasciata.</span><span class="sxs-lookup"><span data-stu-id="e39a7-127">Called after a dialog box displayed by the client control is dismissed.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="e39a7-128">**OnDialogDisplaying**</span><span class="sxs-lookup"><span data-stu-id="e39a7-128">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="e39a7-129">Chiamato prima che il controllo visualizzi una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e39a7-129">Called before the control displays a dialog box.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="e39a7-130">**Disconnected**</span><span class="sxs-lookup"><span data-stu-id="e39a7-130">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="e39a7-131">Chiamato quando il controllo client è stato disconnesso da una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e39a7-131">Called when the client control has been disconnected from a remote session.</span></span> <br/>                                                                             |
| [<span data-ttu-id="e39a7-132">**OnKeyCombinationPressed**</span><span class="sxs-lookup"><span data-stu-id="e39a7-132">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="e39a7-133">Chiamato quando vengono premuti combinazioni di tasti speciali nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e39a7-133">Called when special key combinations are pressed in the remote session.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="e39a7-134">**OnLoginCompleted**</span><span class="sxs-lookup"><span data-stu-id="e39a7-134">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="e39a7-135">Chiamato quando il controllo client ha effettuato correttamente l'accesso a una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="e39a7-135">Called when the client control has successfully logged on to a remote session.</span></span> <br/>                                                                          |
| [<span data-ttu-id="e39a7-136">**OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="e39a7-136">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="e39a7-137">Chiamato quando lo stato della rete è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="e39a7-137">Called when the network status has changed.</span></span> <br/>                                                                                                             |
| [<span data-ttu-id="e39a7-138">**OnRemoteDesktopSizeChanged**</span><span class="sxs-lookup"><span data-stu-id="e39a7-138">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="e39a7-139">Chiamato quando viene modificata la dimensione del desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e39a7-139">Called when the remote desktop size has changed.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="e39a7-140">**OnStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="e39a7-140">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="e39a7-141">Chiamato quando il controllo client ha aggiornato il proprio stato.</span><span class="sxs-lookup"><span data-stu-id="e39a7-141">Called when the client control has updated its status.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="e39a7-142">**OnTouchPointerCursorMoved**</span><span class="sxs-lookup"><span data-stu-id="e39a7-142">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="e39a7-143">Chiamato quando il cursore del puntatore tocco è stato spostato e la proprietà [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="e39a7-143">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="e39a7-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e39a7-144">Requirements</span></span>



| <span data-ttu-id="e39a7-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e39a7-145">Requirement</span></span> | <span data-ttu-id="e39a7-146">Valore</span><span class="sxs-lookup"><span data-stu-id="e39a7-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e39a7-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e39a7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="e39a7-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e39a7-148">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="e39a7-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e39a7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="e39a7-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e39a7-150">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="e39a7-151">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e39a7-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="e39a7-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e39a7-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e39a7-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e39a7-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e39a7-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e39a7-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e39a7-155">CLSID</span><span class="sxs-lookup"><span data-stu-id="e39a7-155">CLSID</span></span><br/>                    | <span data-ttu-id="e39a7-156">CLSID \_ RemoteDesktopClient è definito come EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span><span class="sxs-lookup"><span data-stu-id="e39a7-156">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/>       |
| <span data-ttu-id="e39a7-157">IID</span><span class="sxs-lookup"><span data-stu-id="e39a7-157">IID</span></span><br/>                      | <span data-ttu-id="e39a7-158">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="e39a7-158">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e39a7-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e39a7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e39a7-160">Riferimento al controllo ActiveX Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="e39a7-160">Remote Desktop ActiveX control reference</span></span>](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

