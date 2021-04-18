---
description: Recupera le intestazioni della risposta HTTP.
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: 'Metodo IWinHttpRequest:: GetResponseHeader'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetResponseHeader
- WinHttpRequest.GetResponseHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 6e51b0973c7b078c7de592565db19bf6e029c5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317008"
---
# <a name="iwinhttprequestgetresponseheader-method"></a><span data-ttu-id="60250-103">Metodo IWinHttpRequest:: GetResponseHeader</span><span class="sxs-lookup"><span data-stu-id="60250-103">IWinHttpRequest::GetResponseHeader method</span></span>

<span data-ttu-id="60250-104">Il metodo **getResponseHeader** recupera le intestazioni della risposta http.</span><span class="sxs-lookup"><span data-stu-id="60250-104">The **GetResponseHeader** method retrieves the HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="60250-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60250-105">Syntax</span></span>


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a><span data-ttu-id="60250-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60250-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60250-107">*Intestazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="60250-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60250-108">Specifica il nome dell'intestazione senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="60250-108">Specifies the case-insensitive header name.</span></span>

</dd> <dt>

<span data-ttu-id="60250-109">*Valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="60250-109">*Value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="60250-110">Riceve le informazioni di intestazione risultanti.</span><span class="sxs-lookup"><span data-stu-id="60250-110">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60250-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60250-111">Return value</span></span>

<span data-ttu-id="60250-112">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="60250-112">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="60250-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="60250-113">Remarks</span></span>

<span data-ttu-id="60250-114">Questo metodo restituisce il valore dell'intestazione della risposta denominata in *header*.</span><span class="sxs-lookup"><span data-stu-id="60250-114">This method returns the value of the response header named in *Header*.</span></span> <span data-ttu-id="60250-115">Tenere presente che i client di automazione, ad esempio script, ottengono i dati di intestazione come valore restituito della chiamata di funzione, non tramite un parametro di funzione.</span><span class="sxs-lookup"><span data-stu-id="60250-115">Be aware that automation clients, such as script, get the header data as the return value of the function call, not through a function parameter.</span></span> <span data-ttu-id="60250-116">Richiamare questo metodo solo dopo la chiamata del metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="60250-116">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="60250-117">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="60250-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="60250-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="60250-118">Examples</span></span>

<span data-ttu-id="60250-119">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere l'intestazione della data dalla risposta.</span><span class="sxs-lookup"><span data-stu-id="60250-119">The following example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span> <span data-ttu-id="60250-120">Questo esempio deve essere eseguito da un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="60250-120">This example must be run from a command prompt.</span></span>


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

    // Initialize COM
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

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1",
                         &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {
        // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {
        // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get Response text.
        BSTR bstrName = SysAllocString(L"Date");
        hr = pIWinHttpRequest->GetResponseHeader(bstrName,
                                             &bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print response to console.
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



<span data-ttu-id="60250-121">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere l'intestazione della data dalla risposta.</span><span class="sxs-lookup"><span data-stu-id="60250-121">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", 
                "https://www.microsoft.com", 
                 false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the date header.
WScript.Echo( WinHttpReq.GetResponseHeader("Date"));
```



## <a name="requirements"></a><span data-ttu-id="60250-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60250-122">Requirements</span></span>



| <span data-ttu-id="60250-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60250-123">Requirement</span></span> | <span data-ttu-id="60250-124">Valore</span><span class="sxs-lookup"><span data-stu-id="60250-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="60250-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60250-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60250-126">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="60250-126">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="60250-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60250-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60250-128">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="60250-128">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="60250-129">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="60250-129">Redistributable</span></span><br/>          | <span data-ttu-id="60250-130">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="60250-130">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="60250-131">IDL</span><span class="sxs-lookup"><span data-stu-id="60250-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60250-132"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60250-132"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="60250-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="60250-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="60250-134"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60250-134"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="60250-135">DLL</span><span class="sxs-lookup"><span data-stu-id="60250-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60250-136"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60250-136"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="60250-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60250-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60250-138">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="60250-138">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="60250-139">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="60250-139">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="60250-140">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="60250-140">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[<span data-ttu-id="60250-141">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="60250-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




