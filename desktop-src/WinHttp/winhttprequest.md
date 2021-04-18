---
Description: In questo argomento vengono fornite informazioni sull'utilizzo dell'oggetto COM WinHTTP WinHttpRequest con i linguaggi di scripting.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Oggetto WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328193"
---
# <a name="winhttprequest-object"></a><span data-ttu-id="7350b-103">Oggetto WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="7350b-103">WinHttpRequest object</span></span>

<span data-ttu-id="7350b-104">In questo argomento vengono fornite informazioni sull'utilizzo dell'oggetto com WinHTTP **WinHttpRequest** con i linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="7350b-104">This topic provides information about using the WinHTTP **WinHttpRequest** COM object with scripting languages.</span></span> <span data-ttu-id="7350b-105">Per ulteriori informazioni, tra cui l'API C++ (WinHTTP), consultare [informazioni su WinHTTP](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="7350b-105">For more information, including the C++ API (WinHTTP) please see [About WinHTTP](about-winhttp.md).</span></span> <span data-ttu-id="7350b-106">Vedere [scelta di un'interfaccia WinHTTP](choosing-a-winhttp-interface.md) per un confronto di queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="7350b-106">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span>

## <a name="example"></a><span data-ttu-id="7350b-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="7350b-107">Example</span></span>

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

<span data-ttu-id="7350b-108">Esempi di codice ricavati dalla [Proprietà IWinHttpRequest:: status](iwinhttprequest-status.md).</span><span class="sxs-lookup"><span data-stu-id="7350b-108">Code examples taken from [IWinHttpRequest::Status property](iwinhttprequest-status.md).</span></span>



## <a name="members"></a><span data-ttu-id="7350b-109">Membri</span><span class="sxs-lookup"><span data-stu-id="7350b-109">Members</span></span>

<span data-ttu-id="7350b-110">L'oggetto **WinHttpRequest** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7350b-110">The **WinHttpRequest** object has these types of members:</span></span>

-   [<span data-ttu-id="7350b-111">Eventi</span><span class="sxs-lookup"><span data-stu-id="7350b-111">Events</span></span>](#events)
-   [<span data-ttu-id="7350b-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="7350b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7350b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7350b-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="7350b-114">Eventi</span><span class="sxs-lookup"><span data-stu-id="7350b-114">Events</span></span>

<span data-ttu-id="7350b-115">L'oggetto **WinHttpRequest** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="7350b-115">The **WinHttpRequest** object has these events.</span></span>



| <span data-ttu-id="7350b-116">Event</span><span class="sxs-lookup"><span data-stu-id="7350b-116">Event</span></span>                                                                            | <span data-ttu-id="7350b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7350b-117">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="7350b-118">**OnError**</span><span class="sxs-lookup"><span data-stu-id="7350b-118">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="7350b-119">Si verifica in presenza di un errore di run-time nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7350b-119">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="7350b-120">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="7350b-120">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="7350b-121">Si verifica quando i dati sono disponibili dalla risposta.</span><span class="sxs-lookup"><span data-stu-id="7350b-121">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="7350b-122">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="7350b-122">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="7350b-123">Si verifica quando i dati della risposta sono completi.</span><span class="sxs-lookup"><span data-stu-id="7350b-123">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="7350b-124">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="7350b-124">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="7350b-125">Si verifica quando i dati di risposta iniziano a essere ricevuti.</span><span class="sxs-lookup"><span data-stu-id="7350b-125">Occurs when the response data starts to be received.</span></span><br/>      |



 

### <a name="methods"></a><span data-ttu-id="7350b-126">Metodi</span><span class="sxs-lookup"><span data-stu-id="7350b-126">Methods</span></span>

<span data-ttu-id="7350b-127">L'oggetto **WinHttpRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7350b-127">The **WinHttpRequest** object has these methods.</span></span>



| <span data-ttu-id="7350b-128">Metodo</span><span class="sxs-lookup"><span data-stu-id="7350b-128">Method</span></span>                                                                 | <span data-ttu-id="7350b-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7350b-129">Description</span></span>                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7350b-130">**Interruzione**</span><span class="sxs-lookup"><span data-stu-id="7350b-130">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="7350b-131">Interrompe un metodo di [**invio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="7350b-131">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                                              |
| [<span data-ttu-id="7350b-132">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="7350b-132">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="7350b-133">Recupera tutte le intestazioni di risposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7350b-133">Retrieves all HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="7350b-134">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="7350b-134">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="7350b-135">Recupera le intestazioni della risposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7350b-135">Retrieves the HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="7350b-136">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="7350b-136">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="7350b-137">Apre una connessione HTTP a una risorsa HTTP.</span><span class="sxs-lookup"><span data-stu-id="7350b-137">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="7350b-138">**Invia**</span><span class="sxs-lookup"><span data-stu-id="7350b-138">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="7350b-139">Invia una richiesta HTTP a un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="7350b-139">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="7350b-140">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="7350b-140">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="7350b-141">Imposta i [criteri di accesso automatici](authentication-in-winhttp.md)correnti.</span><span class="sxs-lookup"><span data-stu-id="7350b-141">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                                                |
| [<span data-ttu-id="7350b-142">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="7350b-142">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="7350b-143">Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="7350b-143">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                                    |
| [<span data-ttu-id="7350b-144">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="7350b-144">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="7350b-145">Imposta le credenziali da utilizzare con un server HTTP, un'origine o un server proxy.</span><span class="sxs-lookup"><span data-stu-id="7350b-145">Sets credentials to be used with an HTTP server either an origin or a proxy server.</span></span><br/>                                                             |
| [<span data-ttu-id="7350b-146">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="7350b-146">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="7350b-147">Imposta le informazioni sul server proxy.</span><span class="sxs-lookup"><span data-stu-id="7350b-147">Sets proxy server information.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="7350b-148">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="7350b-148">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="7350b-149">Aggiunge, modifica o Elimina un'intestazione della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7350b-149">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                                               |
| [<span data-ttu-id="7350b-150">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="7350b-150">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="7350b-151">Specifica, in millisecondi, i singoli componenti di timeout di un'operazione di invio/ricezione.</span><span class="sxs-lookup"><span data-stu-id="7350b-151">Specifies, in milliseconds, the individual time-out components of a send/receive operation.</span></span><br/>                                                     |
| [<span data-ttu-id="7350b-152">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="7350b-152">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="7350b-153">Specifica il tempo di attesa, in secondi, per il completamento di un metodo di [**invio**](iwinhttprequest-send.md) asincrono, con un valore di timeout facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7350b-153">Specifies the wait time, in seconds, for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7350b-154">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7350b-154">Properties</span></span>

<span data-ttu-id="7350b-155">L'oggetto **WinHttpRequest** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7350b-155">The **WinHttpRequest** object has these properties.</span></span>



| <span data-ttu-id="7350b-156">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7350b-156">Property</span></span>                                                            | <span data-ttu-id="7350b-157">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="7350b-157">Access type</span></span>           | <span data-ttu-id="7350b-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7350b-158">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="7350b-159">**Opzione**</span><span class="sxs-lookup"><span data-stu-id="7350b-159">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="7350b-160">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7350b-160">Read/write</span></span><br/> | <span data-ttu-id="7350b-161">Imposta o recupera un valore di opzione WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7350b-161">Sets or retrieves a WinHTTP option value.</span></span><br/>                            |
| [<span data-ttu-id="7350b-162">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="7350b-162">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="7350b-163">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7350b-163">Read-only</span></span><br/>  | <span data-ttu-id="7350b-164">Recupera il corpo dell'entità della risposta come matrice di byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="7350b-164">Retrieves the response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="7350b-165">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="7350b-165">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="7350b-166">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7350b-166">Read-only</span></span><br/>  | <span data-ttu-id="7350b-167">Recupera il corpo dell'entità di risposta come [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="7350b-167">Retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="7350b-168">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="7350b-168">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="7350b-169">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7350b-169">Read-only</span></span><br/>  | <span data-ttu-id="7350b-170">Recupera il corpo dell'entità di risposta come testo.</span><span class="sxs-lookup"><span data-stu-id="7350b-170">Retrieves the response entity body as text.</span></span><br/>                          |
| [<span data-ttu-id="7350b-171">**Stato**</span><span class="sxs-lookup"><span data-stu-id="7350b-171">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="7350b-172">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7350b-172">Read-only</span></span><br/>  | <span data-ttu-id="7350b-173">Recupera il codice di stato HTTP dall'ultima risposta.</span><span class="sxs-lookup"><span data-stu-id="7350b-173">Retrieves the HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="7350b-174">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="7350b-174">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="7350b-175">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7350b-175">Read-only</span></span><br/>  | <span data-ttu-id="7350b-176">Recupera il testo di stato HTTP.</span><span class="sxs-lookup"><span data-stu-id="7350b-176">Retrieves HTTP status text.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="7350b-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="7350b-177">Remarks</span></span>

<span data-ttu-id="7350b-178">L'oggetto **WinHttpRequest** utilizza l'interfaccia [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) per fornire i dati di errore.</span><span class="sxs-lookup"><span data-stu-id="7350b-178">The **WinHttpRequest** object uses the [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) interface to provide error data.</span></span> <span data-ttu-id="7350b-179">È possibile ottenere una descrizione e un valore di errore numerico con l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) in Microsoft Visual Basic Scripting Edition (VBScript) e l'oggetto [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) in Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="7350b-179">A description and numerical error value can be obtained with the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object in Microsoft Visual Basic Scripting Edition (VBScript), and the [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) object in Microsoft JScript.</span></span> <span data-ttu-id="7350b-180">I 16 bit inferiori di un numero di errore corrispondono ai valori trovati nei [**messaggi di errore**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="7350b-180">The lower 16 bits of an error number correspond to the values found in [**Error Messages**](error-messages.md).</span></span>

> [!Note]  
> <span data-ttu-id="7350b-181">Per Windows XP e Windows 2000, vedere [requisiti di run-time](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="7350b-181">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7350b-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7350b-182">Requirements</span></span>



| <span data-ttu-id="7350b-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="7350b-183">Requirement</span></span> | <span data-ttu-id="7350b-184">Valore</span><span class="sxs-lookup"><span data-stu-id="7350b-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7350b-185">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7350b-185">Minimum supported client</span></span><br/> | <span data-ttu-id="7350b-186">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="7350b-186">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7350b-187">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7350b-187">Minimum supported server</span></span><br/> | <span data-ttu-id="7350b-188">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="7350b-188">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7350b-189">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7350b-189">Redistributable</span></span><br/>          | <span data-ttu-id="7350b-190">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7350b-190">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7350b-191">IDL</span><span class="sxs-lookup"><span data-stu-id="7350b-191">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7350b-192"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7350b-192"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="7350b-193">Libreria</span><span class="sxs-lookup"><span data-stu-id="7350b-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="7350b-194"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7350b-194"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="7350b-195">DLL</span><span class="sxs-lookup"><span data-stu-id="7350b-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7350b-196"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7350b-196"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7350b-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7350b-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7350b-198">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7350b-198">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

