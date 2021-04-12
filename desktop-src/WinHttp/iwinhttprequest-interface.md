---
description: L'interfaccia IWinHttpRequest fornisce tutti i metodi non uniformi per i servizi HTTP di Microsoft Windows (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interfaccia IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231832"
---
# <a name="iwinhttprequest-interface"></a><span data-ttu-id="98435-103">Interfaccia IWinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="98435-103">IWinHttpRequest interface</span></span>

<span data-ttu-id="98435-104">L'interfaccia **IWinHttpRequest** fornisce tutti i metodi non uniformi per i [Servizi http di Microsoft Windows (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="98435-104">The **IWinHttpRequest** interface provides all of the nonevent methods for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span>

## <a name="members"></a><span data-ttu-id="98435-105">Membri</span><span class="sxs-lookup"><span data-stu-id="98435-105">Members</span></span>

<span data-ttu-id="98435-106">L'interfaccia **IWinHttpRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="98435-106">The **IWinHttpRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="98435-107">**IWinHttpRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="98435-107">**IWinHttpRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="98435-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="98435-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="98435-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="98435-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="98435-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="98435-110">Methods</span></span>

<span data-ttu-id="98435-111">L'interfaccia **IWinHttpRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="98435-111">The **IWinHttpRequest** interface has these methods.</span></span>



| <span data-ttu-id="98435-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="98435-112">Method</span></span>                                                                 | <span data-ttu-id="98435-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98435-113">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98435-114">**Interruzione**</span><span class="sxs-lookup"><span data-stu-id="98435-114">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="98435-115">Interrompe un metodo di [**invio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="98435-115">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                           |
| [<span data-ttu-id="98435-116">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="98435-116">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="98435-117">Recupera tutte le intestazioni di risposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-117">Retrieves all HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="98435-118">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="98435-118">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="98435-119">Recupera le intestazioni della risposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-119">Retrieves the HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="98435-120">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="98435-120">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="98435-121">Apre una connessione HTTP a una risorsa HTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-121">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                |
| [<span data-ttu-id="98435-122">**Invia**</span><span class="sxs-lookup"><span data-stu-id="98435-122">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="98435-123">Invia una richiesta HTTP a un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-123">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                     |
| [<span data-ttu-id="98435-124">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="98435-124">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="98435-125">Imposta i [criteri di accesso automatici](authentication-in-winhttp.md)correnti.</span><span class="sxs-lookup"><span data-stu-id="98435-125">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                             |
| [<span data-ttu-id="98435-126">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="98435-126">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="98435-127">Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="98435-127">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                 |
| [<span data-ttu-id="98435-128">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="98435-128">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="98435-129">Imposta le credenziali da utilizzare con un server HTTP, un server proxy o un server di origine.</span><span class="sxs-lookup"><span data-stu-id="98435-129">Sets credentials to be used with an HTTP server, either a proxy server or an originating server.</span></span><br/>                             |
| [<span data-ttu-id="98435-130">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="98435-130">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="98435-131">Imposta le informazioni sul server proxy.</span><span class="sxs-lookup"><span data-stu-id="98435-131">Sets proxy server information.</span></span><br/>                                                                                               |
| [<span data-ttu-id="98435-132">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="98435-132">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="98435-133">Aggiunge, modifica o Elimina un'intestazione della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-133">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                            |
| [<span data-ttu-id="98435-134">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="98435-134">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="98435-135">Specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="98435-135">Specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span><br/>                                   |
| [<span data-ttu-id="98435-136">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="98435-136">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="98435-137">Attende il completamento di un metodo di [**invio**](iwinhttprequest-send.md) asincrono, con un valore di timeout facoltativo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="98435-137">Waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="98435-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="98435-138">Properties</span></span>

<span data-ttu-id="98435-139">L'interfaccia **IWinHttpRequest** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="98435-139">The **IWinHttpRequest** interface has these properties.</span></span>



| <span data-ttu-id="98435-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="98435-140">Property</span></span>                                                            | <span data-ttu-id="98435-141">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="98435-141">Access type</span></span>           | <span data-ttu-id="98435-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98435-142">Description</span></span>                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="98435-143">**Opzione**</span><span class="sxs-lookup"><span data-stu-id="98435-143">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="98435-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="98435-144">Read/write</span></span><br/> | <span data-ttu-id="98435-145">Valore di opzione WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-145">A WinHTTP option value.</span></span><br/>                                    |
| [<span data-ttu-id="98435-146">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="98435-146">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="98435-147">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="98435-147">Read-only</span></span><br/>  | <span data-ttu-id="98435-148">Corpo dell'entità della risposta come matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="98435-148">The response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="98435-149">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="98435-149">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="98435-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="98435-150">Read-only</span></span><br/>  | <span data-ttu-id="98435-151">Corpo dell'entità della risposta come [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="98435-151">The response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="98435-152">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="98435-152">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="98435-153">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="98435-153">Read-only</span></span><br/>  | <span data-ttu-id="98435-154">Corpo dell'entità della risposta.</span><span class="sxs-lookup"><span data-stu-id="98435-154">The response entity body.</span></span><br/>                                  |
| [<span data-ttu-id="98435-155">**Stato**</span><span class="sxs-lookup"><span data-stu-id="98435-155">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="98435-156">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="98435-156">Read-only</span></span><br/>  | <span data-ttu-id="98435-157">Codice di stato HTTP dell'ultima risposta.</span><span class="sxs-lookup"><span data-stu-id="98435-157">The HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="98435-158">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="98435-158">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="98435-159">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="98435-159">Read-only</span></span><br/>  | <span data-ttu-id="98435-160">Testo di stato HTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-160">The HTTP status text.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="98435-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="98435-161">Remarks</span></span>

<span data-ttu-id="98435-162">L'interfaccia **IWinHttpRequest** definita in HttpRequest. idl è implementata da una classe con ID **CLSID \_ WinHttpRequest**.</span><span class="sxs-lookup"><span data-stu-id="98435-162">The **IWinHttpRequest** interface defined in httprequest.idl is implemented by a class with id of **CLSID\_WinHttpRequest**.</span></span> <span data-ttu-id="98435-163">Un'applicazione ottiene questa interfaccia chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un ID di classe **CLSID \_ WinHttpRequest** e un ID di interfaccia **IID \_ IWinHttpRequest**.</span><span class="sxs-lookup"><span data-stu-id="98435-163">An application obtain this interface by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class id of **CLSID\_WinHttpRequest** and an interface id of **IID\_IWinHttpRequest**.</span></span>

> [!Note]  
> <span data-ttu-id="98435-164">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="98435-164">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98435-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98435-165">Requirements</span></span>



| <span data-ttu-id="98435-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="98435-166">Requirement</span></span> | <span data-ttu-id="98435-167">Valore</span><span class="sxs-lookup"><span data-stu-id="98435-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="98435-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98435-168">Minimum supported client</span></span><br/> | <span data-ttu-id="98435-169">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="98435-169">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="98435-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98435-170">Minimum supported server</span></span><br/> | <span data-ttu-id="98435-171">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="98435-171">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="98435-172">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="98435-172">Redistributable</span></span><br/>          | <span data-ttu-id="98435-173">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="98435-173">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="98435-174">IDL</span><span class="sxs-lookup"><span data-stu-id="98435-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98435-175"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98435-175"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="98435-176">Libreria</span><span class="sxs-lookup"><span data-stu-id="98435-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="98435-177"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98435-177"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="98435-178">DLL</span><span class="sxs-lookup"><span data-stu-id="98435-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98435-179"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98435-179"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="98435-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98435-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98435-181">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="98435-181">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="98435-182">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="98435-182">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

