---
description: Recupera tutte le intestazioni di risposta HTTP.
ms.assetid: 68b13d4c-5afd-486d-8b78-a7eef0f59a24
title: 'Metodo IWinHttpRequest:: GetAllResponseHeaders'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetAllResponseHeaders
- WinHttpRequest.GetAllResponseHeaders
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 74c113216cf41e2f9816176dd28ba5e84208c635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317010"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a><span data-ttu-id="59238-103">Metodo IWinHttpRequest:: GetAllResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="59238-103">IWinHttpRequest::GetAllResponseHeaders method</span></span>

<span data-ttu-id="59238-104">Il metodo **GetAllResponseHeaders** recupera tutte le intestazioni di risposta http.</span><span class="sxs-lookup"><span data-stu-id="59238-104">The **GetAllResponseHeaders** method retrieves all HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="59238-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59238-105">Syntax</span></span>


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a><span data-ttu-id="59238-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59238-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59238-107">*Intestazioni* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="59238-107">*Headers* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="59238-108">Riceve le informazioni di intestazione risultanti.</span><span class="sxs-lookup"><span data-stu-id="59238-108">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59238-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59238-109">Return value</span></span>

<span data-ttu-id="59238-110">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="59238-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="59238-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="59238-111">Remarks</span></span>

<span data-ttu-id="59238-112">Questo metodo restituisce tutte le intestazioni contenute nella risposta server più recente.</span><span class="sxs-lookup"><span data-stu-id="59238-112">This method returns all of the headers contained in the most recent server response.</span></span> <span data-ttu-id="59238-113">Le singole intestazioni sono delimitate da una combinazione di ritorno a capo e avanzamento riga (ASCII 13 e 10).</span><span class="sxs-lookup"><span data-stu-id="59238-113">The individual headers are delimited by a carriage return and line feed combination (ASCII 13 and 10).</span></span> <span data-ttu-id="59238-114">L'ultima voce è seguita da due delimitatori (13, 10, 13, 10).</span><span class="sxs-lookup"><span data-stu-id="59238-114">The last entry is followed by two delimiters (13, 10, 13, 10).</span></span> <span data-ttu-id="59238-115">Richiamare questo metodo solo dopo la chiamata del metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="59238-115">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="59238-116">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="59238-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="59238-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="59238-117">Examples</span></span>

<span data-ttu-id="59238-118">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere tutte le intestazioni dalla risposta.</span><span class="sxs-lookup"><span data-stu-id="59238-118">The following example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span> <span data-ttu-id="59238-119">Questo esempio deve essere eseguito da un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="59238-119">This example should be run from a command prompt.</span></span>


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

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

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
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
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



<span data-ttu-id="59238-120">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere tutte le intestazioni dalla risposta.</span><span class="sxs-lookup"><span data-stu-id="59238-120">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Get all response headers.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="59238-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59238-121">Requirements</span></span>



| <span data-ttu-id="59238-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="59238-122">Requirement</span></span> | <span data-ttu-id="59238-123">Valore</span><span class="sxs-lookup"><span data-stu-id="59238-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="59238-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59238-124">Minimum supported client</span></span><br/> | <span data-ttu-id="59238-125">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="59238-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="59238-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59238-126">Minimum supported server</span></span><br/> | <span data-ttu-id="59238-127">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="59238-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="59238-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="59238-128">Redistributable</span></span><br/>          | <span data-ttu-id="59238-129">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="59238-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="59238-130">IDL</span><span class="sxs-lookup"><span data-stu-id="59238-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59238-131"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59238-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="59238-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="59238-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="59238-133"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59238-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="59238-134">DLL</span><span class="sxs-lookup"><span data-stu-id="59238-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59238-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59238-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="59238-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59238-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59238-137">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="59238-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="59238-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="59238-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="59238-139">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="59238-139">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[<span data-ttu-id="59238-140">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="59238-140">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




