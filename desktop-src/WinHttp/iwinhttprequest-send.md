---
description: Il metodo Send invia una richiesta HTTP a un server HTTP.
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: 'Metodo IWinHttpRequest:: Send'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Send
- WinHttpRequest.Send
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0040ed6c09814a2b2112a91173d84430b8130a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758330"
---
# <a name="iwinhttprequestsend-method"></a><span data-ttu-id="d8e53-103">Metodo IWinHttpRequest:: Send</span><span class="sxs-lookup"><span data-stu-id="d8e53-103">IWinHttpRequest::Send method</span></span>

<span data-ttu-id="d8e53-104">Il metodo **Send** invia una richiesta HTTP a un server http.</span><span class="sxs-lookup"><span data-stu-id="d8e53-104">The **Send** method sends an HTTP request to an HTTP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8e53-105">Syntax</span></span>


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a><span data-ttu-id="d8e53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8e53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8e53-107">*Corpo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d8e53-107">*Body* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e53-108">Dati da inviare al server.</span><span class="sxs-lookup"><span data-stu-id="d8e53-108">Data to be sent to the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8e53-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8e53-109">Return value</span></span>

<span data-ttu-id="d8e53-110">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="d8e53-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e53-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8e53-111">Remarks</span></span>

<span data-ttu-id="d8e53-112">La richiesta da inviare è stata definita in una chiamata precedente al metodo [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e53-112">The request to be sent was defined in a prior call to the [**Open**](iwinhttprequest-open.md) method.</span></span> <span data-ttu-id="d8e53-113">L'applicazione chiamante può fornire i dati da inviare al server tramite il parametro *Body* .</span><span class="sxs-lookup"><span data-stu-id="d8e53-113">The calling application can provide data to be sent to the server through the *Body* parameter.</span></span> <span data-ttu-id="d8e53-114">Se il [*verbo http*](glossary.md) dell'oggetto [**aperto**](iwinhttprequest-open.md) è "Get", questo metodo Invia la richiesta senza *corpo*, anche se viene fornita dall'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="d8e53-114">If the [*HTTP verb*](glossary.md) of the object's [**Open**](iwinhttprequest-open.md) is "GET", this method sends the request without *Body*, even if it is provided by the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="d8e53-115">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d8e53-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d8e53-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="d8e53-116">Examples</span></span>

<span data-ttu-id="d8e53-117">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="d8e53-117">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;

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
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print response to console.
    wprintf(L"%.256s",bstrResponse);

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="d8e53-118">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="d8e53-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



<span data-ttu-id="d8e53-119">Nell'esempio di script seguente viene illustrato come inserire dati in un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="d8e53-119">The following scripting example shows how to post data to an HTTP server.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a><span data-ttu-id="d8e53-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8e53-120">Requirements</span></span>



| <span data-ttu-id="d8e53-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e53-121">Requirement</span></span> | <span data-ttu-id="d8e53-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d8e53-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e53-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8e53-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e53-124">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="d8e53-124">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="d8e53-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8e53-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e53-126">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="d8e53-126">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="d8e53-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d8e53-127">Redistributable</span></span><br/>          | <span data-ttu-id="d8e53-128">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d8e53-128">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="d8e53-129">IDL</span><span class="sxs-lookup"><span data-stu-id="d8e53-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8e53-130"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8e53-130"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="d8e53-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8e53-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8e53-132"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8e53-132"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="d8e53-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d8e53-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8e53-134"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8e53-134"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d8e53-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8e53-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e53-136">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d8e53-136">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="d8e53-137">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d8e53-137">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="d8e53-138">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d8e53-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




