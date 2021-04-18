---
description: Il metodo WaitForResponse attende il completamento di un metodo Send asincrono, con un valore di timeout facoltativo, in secondi.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: 'Metodo IWinHttpRequest:: WaitForResponse'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317005"
---
# <a name="iwinhttprequestwaitforresponse-method"></a><span data-ttu-id="4606d-103">Metodo IWinHttpRequest:: WaitForResponse</span><span class="sxs-lookup"><span data-stu-id="4606d-103">IWinHttpRequest::WaitForResponse method</span></span>

<span data-ttu-id="4606d-104">Il metodo **waitForResponse** attende il completamento di un metodo [**Send**](iwinhttprequest-send.md) asincrono, con un valore di timeout facoltativo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="4606d-104">The **WaitForResponse** method waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4606d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4606d-105">Syntax</span></span>


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a><span data-ttu-id="4606d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4606d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4606d-107">*Timeout* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4606d-107">*Timeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4606d-108">Valore di timeout, in secondi.</span><span class="sxs-lookup"><span data-stu-id="4606d-108">Time-out value, in seconds.</span></span> <span data-ttu-id="4606d-109">Il timeout predefinito è infinito.</span><span class="sxs-lookup"><span data-stu-id="4606d-109">Default time-out is infinite.</span></span> <span data-ttu-id="4606d-110">Per impostare in modo esplicito il timeout su infinito, utilizzare il valore-1.</span><span class="sxs-lookup"><span data-stu-id="4606d-110">To explicitly set time-out to infinite, use the value -1.</span></span>

</dd> <dt>

<span data-ttu-id="4606d-111">Operazione *riuscita* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4606d-111">*Succeeded* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4606d-112">Riceve uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4606d-112">Receives one of the following values.</span></span>



| <span data-ttu-id="4606d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4606d-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="4606d-114">Significato</span><span class="sxs-lookup"><span data-stu-id="4606d-114">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="4606d-115"><dt>**VARIANT \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="4606d-115"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="4606d-116">È stata ricevuta una risposta.</span><span class="sxs-lookup"><span data-stu-id="4606d-116">A response has been received.</span></span><br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="4606d-117"><dt>**VARIANTE \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4606d-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4606d-118">È stato superato il periodo di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="4606d-118">The specified time-out period was exceeded.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4606d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4606d-119">Return value</span></span>

<span data-ttu-id="4606d-120">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="4606d-120">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4606d-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="4606d-121">Remarks</span></span>

<span data-ttu-id="4606d-122">Questo metodo sospende l'esecuzione in attesa di una risposta a una richiesta asincrona.</span><span class="sxs-lookup"><span data-stu-id="4606d-122">This method suspends execution while waiting for a response to an asynchronous request.</span></span> <span data-ttu-id="4606d-123">Questo metodo deve essere chiamato dopo un'operazione [**Send**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="4606d-123">This method should be called after a [**Send**](iwinhttprequest-send.md).</span></span> <span data-ttu-id="4606d-124">La chiamata di applicazioni può specificare un valore di *timeout* facoltativo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="4606d-124">Calling applications can specify an optional *Timeout* value, in seconds.</span></span> <span data-ttu-id="4606d-125">Se si verifica il timeout di questo metodo, la richiesta non viene interrotta.</span><span class="sxs-lookup"><span data-stu-id="4606d-125">If this method times out, the request is not aborted.</span></span> <span data-ttu-id="4606d-126">In questo modo, l'applicazione chiamante può continuare ad attendere la richiesta, se necessario, in una chiamata successiva a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4606d-126">This way, the calling application can continue to wait for the request, if desired, in a subsequent call to this method.</span></span>

<span data-ttu-id="4606d-127">La chiamata di questa proprietà dopo un metodo di [**invio**](iwinhttprequest-send.md) sincrono viene restituita immediatamente e non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="4606d-127">Calling this property after a synchronous [**Send**](iwinhttprequest-send.md) method returns immediately and has no effect.</span></span>

> [!Note]  
> <span data-ttu-id="4606d-128">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4606d-128">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4606d-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="4606d-129">Examples</span></span>

<span data-ttu-id="4606d-130">Nell'esempio seguente viene illustrato come aprire una connessione HTTP asincrona, inviare una richiesta HTTP, attendere la risposta e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="4606d-130">The following example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for the response and read the response text.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print the response to a console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="4606d-131">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP asincrona, inviare una richiesta HTTP, attendere una risposta e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="4606d-131">The following scripting example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for a response, and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="4606d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4606d-132">Requirements</span></span>



| <span data-ttu-id="4606d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4606d-133">Requirement</span></span> | <span data-ttu-id="4606d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4606d-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4606d-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4606d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4606d-136">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="4606d-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4606d-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4606d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4606d-138">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="4606d-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4606d-139">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4606d-139">Redistributable</span></span><br/>          | <span data-ttu-id="4606d-140">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4606d-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4606d-141">IDL</span><span class="sxs-lookup"><span data-stu-id="4606d-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4606d-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4606d-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4606d-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="4606d-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="4606d-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4606d-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4606d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4606d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4606d-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4606d-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4606d-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4606d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4606d-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4606d-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4606d-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4606d-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4606d-150">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="4606d-150">**Open**</span></span>](iwinhttprequest-open.md)
</dt> <dt>

[<span data-ttu-id="4606d-151">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4606d-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




