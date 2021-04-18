---
description: Fornisce eventi per i servizi HTTP di Microsoft Windows (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interfaccia IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317004"
---
# <a name="iwinhttprequestevents-interface"></a><span data-ttu-id="4dbf6-103">Interfaccia IWinHttpRequestEvents</span><span class="sxs-lookup"><span data-stu-id="4dbf6-103">IWinHttpRequestEvents interface</span></span>

<span data-ttu-id="4dbf6-104">L'interfaccia **IWinHttpRequestEvents** fornisce eventi per i [Servizi http di Microsoft Windows (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbf6-104">The **IWinHttpRequestEvents** interface provides events for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span> <span data-ttu-id="4dbf6-105">USA solo metodi di evento.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-105">It uses only event methods.</span></span>

## <a name="members"></a><span data-ttu-id="4dbf6-106">Membri</span><span class="sxs-lookup"><span data-stu-id="4dbf6-106">Members</span></span>

<span data-ttu-id="4dbf6-107">L'interfaccia **IWinHttpRequestEvents** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4dbf6-107">The **IWinHttpRequestEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4dbf6-108">**IWinHttpRequestEvents** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4dbf6-108">**IWinHttpRequestEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="4dbf6-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="4dbf6-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4dbf6-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="4dbf6-110">Methods</span></span>

<span data-ttu-id="4dbf6-111">L'interfaccia **IWinHttpRequestEvents** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-111">The **IWinHttpRequestEvents** interface has these methods.</span></span>



| <span data-ttu-id="4dbf6-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="4dbf6-112">Method</span></span>                                                                           | <span data-ttu-id="4dbf6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dbf6-113">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="4dbf6-114">**OnError**</span><span class="sxs-lookup"><span data-stu-id="4dbf6-114">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="4dbf6-115">Si verifica in presenza di un errore di run-time nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-115">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="4dbf6-116">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="4dbf6-116">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="4dbf6-117">Si verifica quando i dati sono disponibili dalla risposta.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-117">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="4dbf6-118">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="4dbf6-118">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="4dbf6-119">Si verifica quando i dati della risposta sono completi.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-119">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="4dbf6-120">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="4dbf6-120">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="4dbf6-121">Si verifica quando i dati di risposta iniziano a essere ricevuti.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-121">Occurs when the response data starts to be received.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="4dbf6-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="4dbf6-122">Remarks</span></span>

<span data-ttu-id="4dbf6-123">Nella procedura riportata di seguito viene descritto come eseguire la registrazione per le notifiche.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-123">The following procedure describes how to register for notifications.</span></span>

1.  <span data-ttu-id="4dbf6-124">Ottenere un'interfaccia [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) chiamando **QueryInterface** su un oggetto [**IWinHttpRequest**](iwinhttprequest-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="4dbf6-124">Get an [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface by calling **QueryInterface** on an [**IWinHttpRequest**](iwinhttprequest-interface.md) object.</span></span>
2.  <span data-ttu-id="4dbf6-125">Chiamare [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) sull'interfaccia restituita e passare **IID \_ IWinHttpRequestEvents** a *riid*.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-125">Call [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) on the returned interface and pass **IID\_IWinHttpRequestEvents** to *riid*.</span></span>
3.  <span data-ttu-id="4dbf6-126">Chiamare [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) sul punto di connessione restituito e passare un puntatore a un'interfaccia **IUnknown** su un oggetto che implementa **IWinHttpRequestEvents** in *punk*.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-126">Call [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) on the returned connection point and pass a pointer to an **IUnknown** interface on an object that implements **IWinHttpRequestEvents** to *pUnk*.</span></span>

<span data-ttu-id="4dbf6-127">È possibile terminare le notifiche chiamando [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) sul punto di connessione restituito nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-127">Notifications can be terminated by calling [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) on the connection point returned in step 2.</span></span>

<span data-ttu-id="4dbf6-128">Per visualizzare il codice che registra per le notifiche COM, vedere la sezione client dell'articolo [punti di connessione com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .</span><span class="sxs-lookup"><span data-stu-id="4dbf6-128">To view some code that registers for COM notifications, see the Client section of the [COM Connection Points](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) article.</span></span>

> [!Note]  
> <span data-ttu-id="4dbf6-129">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-129">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4dbf6-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dbf6-130">Requirements</span></span>



| <span data-ttu-id="4dbf6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dbf6-131">Requirement</span></span> | <span data-ttu-id="4dbf6-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4dbf6-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dbf6-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dbf6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4dbf6-134">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="4dbf6-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4dbf6-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dbf6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4dbf6-136">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="4dbf6-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4dbf6-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4dbf6-137">Redistributable</span></span><br/>          | <span data-ttu-id="4dbf6-138">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4dbf6-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4dbf6-139">IDL</span><span class="sxs-lookup"><span data-stu-id="4dbf6-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4dbf6-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4dbf6-140"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dbf6-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dbf6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dbf6-142">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4dbf6-142">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4dbf6-143">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4dbf6-143">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

