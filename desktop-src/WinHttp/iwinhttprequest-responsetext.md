---
description: Recupera il corpo dell'entità di risposta come testo.
ms.assetid: 87caf64f-be11-45c9-af1e-997a55c5e76e
title: 'Proprietà IWinHttpRequest:: ResponseText'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseText
- IWinHttpRequest.get_ResponseText
- WinHttpRequest.ResponseText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 93e0a9b17ba356f9ce6b038be114f5f2c9804eab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316006"
---
# <a name="iwinhttprequestresponsetext-property"></a><span data-ttu-id="523b9-103">Proprietà IWinHttpRequest:: ResponseText</span><span class="sxs-lookup"><span data-stu-id="523b9-103">IWinHttpRequest::ResponseText property</span></span>

<span data-ttu-id="523b9-104">La proprietà **ResponseText** Recupera il corpo dell'entità della risposta come testo.</span><span class="sxs-lookup"><span data-stu-id="523b9-104">The **ResponseText** property retrieves the response entity body as text.</span></span>

<span data-ttu-id="523b9-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="523b9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="523b9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="523b9-106">Syntax</span></span>


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a><span data-ttu-id="523b9-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="523b9-107">Property value</span></span>

<span data-ttu-id="523b9-108">**BSTR** che riceve il corpo dell'entità della risposta come testo.</span><span class="sxs-lookup"><span data-stu-id="523b9-108">**BSTR** that receives the entity body of the response as text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="523b9-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="523b9-109">Error codes</span></span>

<span data-ttu-id="523b9-110">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="523b9-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="523b9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="523b9-111">Remarks</span></span>

<span data-ttu-id="523b9-112">Questa proprietà può essere richiamata solo dopo la chiamata del metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="523b9-112">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

<span data-ttu-id="523b9-113">Quando si usa questa proprietà in modalità sincrona, il limite al numero di caratteri restituito è approssimativamente 2.169.895.</span><span class="sxs-lookup"><span data-stu-id="523b9-113">When using this property in synchronous mode, the limit to the number of characters it returns is approximately 2,169,895.</span></span>

> [!Note]  
> <span data-ttu-id="523b9-114">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="523b9-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="523b9-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="523b9-115">Examples</span></span>

<span data-ttu-id="523b9-116">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="523b9-116">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="523b9-117">Questo esempio deve essere eseguito da un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="523b9-117">This example must be run from a command prompt.</span></span>


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
    {   // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print the response to a console.
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



<span data-ttu-id="523b9-118">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="523b9-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="523b9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="523b9-119">Requirements</span></span>



| <span data-ttu-id="523b9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="523b9-120">Requirement</span></span> | <span data-ttu-id="523b9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="523b9-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="523b9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="523b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="523b9-123">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="523b9-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="523b9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="523b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="523b9-125">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="523b9-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="523b9-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="523b9-126">Redistributable</span></span><br/>          | <span data-ttu-id="523b9-127">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="523b9-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="523b9-128">IDL</span><span class="sxs-lookup"><span data-stu-id="523b9-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="523b9-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="523b9-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="523b9-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="523b9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="523b9-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="523b9-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="523b9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="523b9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="523b9-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="523b9-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="523b9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="523b9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523b9-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="523b9-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="523b9-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="523b9-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="523b9-137">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="523b9-137">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="523b9-138">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="523b9-138">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="523b9-139">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="523b9-139">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




