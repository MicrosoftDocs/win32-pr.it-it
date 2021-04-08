---
description: Recupera il testo di stato HTTP.
ms.assetid: 480babbd-432c-4722-98df-a73ba5928e1f
title: 'Proprietà IWinHttpRequest:: StatusText'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.StatusText
- IWinHttpRequest.get_StatusText
- WinHttpRequest.StatusText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 41288d87b8194caf3a2a14cc89cd5acbffec902c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058347"
---
# <a name="iwinhttprequeststatustext-property"></a><span data-ttu-id="0b619-103">Proprietà IWinHttpRequest:: StatusText</span><span class="sxs-lookup"><span data-stu-id="0b619-103">IWinHttpRequest::StatusText property</span></span>

<span data-ttu-id="0b619-104">La proprietà **StatusText** Recupera il testo di stato http.</span><span class="sxs-lookup"><span data-stu-id="0b619-104">The **StatusText** property retrieves the HTTP status text.</span></span>

<span data-ttu-id="0b619-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0b619-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b619-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b619-106">Syntax</span></span>


```C++
HRESULT get_StatusText(
  [out, retval] BSTR *Status
);
```


```JScript

StatusText = WinHttpRequest.StatusText
```





## <a name="property-value"></a><span data-ttu-id="0b619-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0b619-107">Property value</span></span>

<span data-ttu-id="0b619-108">**BSTR** che riceve il testo di stato http.</span><span class="sxs-lookup"><span data-stu-id="0b619-108">**BSTR** that receives the HTTP status text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b619-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0b619-109">Error codes</span></span>

<span data-ttu-id="0b619-110">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="0b619-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b619-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b619-111">Remarks</span></span>

<span data-ttu-id="0b619-112">Recupera la parte di testo della riga di risposta del server, rendendo disponibile l'equivalente "intuitivo" del codice di stato HTTP numerico.</span><span class="sxs-lookup"><span data-stu-id="0b619-112">Retrieves the text portion of the server response line, making available the "user-friendly" equivalent to the numeric HTTP status code.</span></span> <span data-ttu-id="0b619-113">I risultati di questa proprietà sono validi solo dopo che il metodo [**Send**](iwinhttprequest-send.md) è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0b619-113">The results of this property are valid only after the [**Send**](iwinhttprequest-send.md) method has successfully completed.</span></span>

> [!Note]  
> <span data-ttu-id="0b619-114">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="0b619-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0b619-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b619-115">Examples</span></span>

<span data-ttu-id="0b619-116">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP, visualizzare lo [**stato**](iwinhttprequest-status.md) e **StatusText** e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="0b619-116">The following example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response text.</span></span> <span data-ttu-id="0b619-117">Questo esempio deve essere eseguito da un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="0b619-117">This example must be run from a command prompt.</span></span>


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
    VARIANT         varFalse;
    VARIANT         varEmpty;
    LONG            lStatus = 0;
    BSTR            bstrStatusText = NULL;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

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
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->get_Status(&lStatus);
        hr = pIWinHttpRequest->get_StatusText(&bstrStatusText);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%s\n\n", bstrResponse);
        wprintf(L"%u - %s\n\n", lStatus, bstrStatusText);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrStatusText)
        SysFreeString(bstrStatusText);
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="0b619-118">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP, visualizzare lo [**stato**](iwinhttprequest-status.md) e **StatusText** e leggere le intestazioni della risposta.</span><span class="sxs-lookup"><span data-stu-id="0b619-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response headers.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the status.
WScript.Echo( WinHttpReq.Status + " - " + WinHttpReq.StatusText);

// Display the date header.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="0b619-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b619-119">Requirements</span></span>



| <span data-ttu-id="0b619-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b619-120">Requirement</span></span> | <span data-ttu-id="0b619-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0b619-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b619-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b619-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0b619-123">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="0b619-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0b619-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b619-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0b619-125">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="0b619-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="0b619-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0b619-126">Redistributable</span></span><br/>          | <span data-ttu-id="0b619-127">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0b619-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="0b619-128">IDL</span><span class="sxs-lookup"><span data-stu-id="0b619-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b619-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b619-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="0b619-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b619-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b619-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b619-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="0b619-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0b619-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b619-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b619-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0b619-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b619-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b619-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="0b619-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="0b619-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="0b619-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="0b619-137">**Stato**</span><span class="sxs-lookup"><span data-stu-id="0b619-137">**Status**</span></span>](iwinhttprequest-status.md)
</dt> <dt>

[<span data-ttu-id="0b619-138">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0b619-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




