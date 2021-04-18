---
description: Aggiunge, modifica o Elimina un'intestazione della richiesta HTTP.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: 'Metodo IWinHttpRequest:: SetRequestHeader'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetRequestHeader
- WinHttpRequest.SetRequestHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 9bc2ae6df420f38d11fb2f0f19d5fcbd0bcc0909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319332"
---
# <a name="iwinhttprequestsetrequestheader-method"></a><span data-ttu-id="0fe06-103">Metodo IWinHttpRequest:: SetRequestHeader</span><span class="sxs-lookup"><span data-stu-id="0fe06-103">IWinHttpRequest::SetRequestHeader method</span></span>

<span data-ttu-id="0fe06-104">Il metodo **setRequestHeader** aggiunge, modifica o Elimina un'intestazione della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="0fe06-104">The **SetRequestHeader** method adds, changes, or deletes an HTTP request header.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fe06-105">Syntax</span></span>


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a><span data-ttu-id="0fe06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fe06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fe06-107">*Intestazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0fe06-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fe06-108">Specifica il nome dell'intestazione da impostare, ad esempio "Depth".</span><span class="sxs-lookup"><span data-stu-id="0fe06-108">Specifies the name of the header to be set, for example, "depth".</span></span> <span data-ttu-id="0fe06-109">Questo parametro non deve contenere i due punti e deve essere il testo effettivo dell'intestazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="0fe06-109">This parameter should not contain a colon and must be the actual text of the HTTP header.</span></span>

</dd> <dt>

<span data-ttu-id="0fe06-110">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0fe06-110">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fe06-111">Specifica il valore dell'intestazione, ad esempio "Infinity".</span><span class="sxs-lookup"><span data-stu-id="0fe06-111">Specifies the value of the header, for example, "infinity".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fe06-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fe06-112">Return value</span></span>

<span data-ttu-id="0fe06-113">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="0fe06-113">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe06-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fe06-114">Remarks</span></span>

<span data-ttu-id="0fe06-115">Le intestazioni vengono trasferite tra reindirizzamenti.</span><span class="sxs-lookup"><span data-stu-id="0fe06-115">Headers are transferred across redirects.</span></span> <span data-ttu-id="0fe06-116">Questo può creare una vulnerabilità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0fe06-116">This can create a security vulnerability.</span></span> <span data-ttu-id="0fe06-117">Per evitare che vengano trasferiti intestazioni se si verifica un reindirizzamento, usare il callback [*\_ dello \_ stato WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) per correggere le intestazioni specifiche quando si verifica un reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="0fe06-117">To avoid having headers transferred if a redirect occurs, use the [*WINHTTP\_STATUS\_CALLBACK*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) callback to correct the specific headers when a redirect occurs.</span></span>

<span data-ttu-id="0fe06-118">Il metodo **setRequestHeader** consente all'applicazione chiamante di aggiungere o eliminare un'intestazione di richiesta HTTP prima di inviare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0fe06-118">The **SetRequestHeader** method enables the calling application to add or delete an HTTP request header prior to sending the request.</span></span> <span data-ttu-id="0fe06-119">Il nome dell'intestazione viene specificato nell' *intestazione* e il valore o il token di intestazione viene specificato in *valore*.</span><span class="sxs-lookup"><span data-stu-id="0fe06-119">The header name is given in *Header*, and the header token or value is given in *Value*.</span></span> <span data-ttu-id="0fe06-120">Per aggiungere un'intestazione, fornire un nome e un valore di intestazione.</span><span class="sxs-lookup"><span data-stu-id="0fe06-120">To add a header, supply a header name and value.</span></span> <span data-ttu-id="0fe06-121">Se esiste già un'altra intestazione con questo nome, questa viene sostituita.</span><span class="sxs-lookup"><span data-stu-id="0fe06-121">If another header already exists with this name, it is replaced.</span></span> <span data-ttu-id="0fe06-122">Per eliminare un'intestazione, impostare l' *intestazione* sul nome dell'intestazione da eliminare e impostare il *valore* su **null**.</span><span class="sxs-lookup"><span data-stu-id="0fe06-122">To delete a header, set *Header* to the name of the header to delete and set *Value* to **NULL**.</span></span>

<span data-ttu-id="0fe06-123">Il nome e il valore delle intestazioni della richiesta aggiunti con questo metodo vengono convalidati.</span><span class="sxs-lookup"><span data-stu-id="0fe06-123">The name and value of request headers added with this method are validated.</span></span> <span data-ttu-id="0fe06-124">Le intestazioni devono essere ben formate.</span><span class="sxs-lookup"><span data-stu-id="0fe06-124">Headers must be well formed.</span></span> <span data-ttu-id="0fe06-125">Per ulteriori informazioni sulle intestazioni HTTP valide, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="0fe06-125">For more information about valid HTTP headers, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="0fe06-126">Se viene utilizzata un'intestazione non valida, si verifica un errore e l'intestazione non viene aggiunta.</span><span class="sxs-lookup"><span data-stu-id="0fe06-126">If an invalid header is used, an error occurs and the header is not added.</span></span>

> [!Note]  
> <span data-ttu-id="0fe06-127">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="0fe06-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0fe06-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="0fe06-128">Examples</span></span>

<span data-ttu-id="0fe06-129">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, impostare un'intestazione di richiesta, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="0fe06-129">The following example shows how to open an HTTP connection, set a request header, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="0fe06-130">Questo esempio deve essere eseguito da un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="0fe06-130">This example must be run from a command prompt.</span></span>


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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set request header.
        BSTR bstrName  = SysAllocString(L"Date");
        BSTR bstrValue = SysAllocString(L"Fri, 16 Mar 2001 00:25:54 GMT");
        hr = pIWinHttpRequest->SetRequestHeader(bstrName, bstrValue);
        SysFreeString(bstrName);
        SysFreeString(bstrValue);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response headers.
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



<span data-ttu-id="0fe06-131">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, impostare un'intestazione di richiesta e inviare una richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="0fe06-131">The following scripting example shows how to open an HTTP connection, set a request header, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Add/replace a request header.
WinHttpReq.SetRequestHeader("Date", Date());

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="0fe06-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fe06-132">Requirements</span></span>



| <span data-ttu-id="0fe06-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fe06-133">Requirement</span></span> | <span data-ttu-id="0fe06-134">Valore</span><span class="sxs-lookup"><span data-stu-id="0fe06-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe06-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fe06-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe06-136">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="0fe06-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0fe06-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fe06-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe06-138">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="0fe06-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="0fe06-139">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0fe06-139">Redistributable</span></span><br/>          | <span data-ttu-id="0fe06-140">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0fe06-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="0fe06-141">IDL</span><span class="sxs-lookup"><span data-stu-id="0fe06-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fe06-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fe06-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="0fe06-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fe06-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="0fe06-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fe06-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="0fe06-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0fe06-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fe06-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fe06-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0fe06-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fe06-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe06-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="0fe06-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="0fe06-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="0fe06-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="0fe06-150">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="0fe06-150">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

