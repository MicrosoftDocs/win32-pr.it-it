---
description: Apre una connessione HTTP a una risorsa HTTP.
ms.assetid: 5207e873-44c0-4eeb-9db8-d8b69432070c
title: 'Metodo IWinHttpRequest:: Open'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Open
- WinHttpRequest.Open
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5543832eb1ebc3df210237eff71d415de14b2f62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314112"
---
# <a name="iwinhttprequestopen-method"></a><span data-ttu-id="cd3ae-103">Metodo IWinHttpRequest:: Open</span><span class="sxs-lookup"><span data-stu-id="cd3ae-103">IWinHttpRequest::Open method</span></span>

<span data-ttu-id="cd3ae-104">Il metodo **Open** apre una connessione HTTP a una risorsa http.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-104">The **Open** method opens an HTTP connection to an HTTP resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd3ae-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a><span data-ttu-id="cd3ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd3ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd3ae-107">*Metodo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd3ae-107">*Method* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3ae-108">Specifica il [*verbo http*](glossary.md) usato per il metodo **Open** , ad esempio "Get" o "put".</span><span class="sxs-lookup"><span data-stu-id="cd3ae-108">Specifies the [*HTTP verb*](glossary.md) used for the **Open** method, such as "GET" or "PUT".</span></span> <span data-ttu-id="cd3ae-109">Usare sempre maiuscole perché alcuni server ignorano i *verbi HTTP* minuscoli.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-109">Always use uppercase as some servers ignore lowercase *HTTP verb* s.</span></span>

</dd> <dt>

<span data-ttu-id="cd3ae-110">*URL* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cd3ae-110">*Url* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3ae-111">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-111">Specifies the name of the resource.</span></span> <span data-ttu-id="cd3ae-112">Deve essere un URL assoluto.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-112">This must be an absolute URL.</span></span>

</dd> <dt>

<span data-ttu-id="cd3ae-113">*Asincrono* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="cd3ae-113">*Async* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3ae-114">Indica se aprire in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-114">Indicates whether to open in asynchronous mode.</span></span>



| <span data-ttu-id="cd3ae-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cd3ae-115">Value</span></span>                                                                                                                                                         | <span data-ttu-id="cd3ae-116">Significato</span><span class="sxs-lookup"><span data-stu-id="cd3ae-116">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="cd3ae-117"><dt>**VARIANTE \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cd3ae-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cd3ae-118">Apre la connessione HTTP in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-118">Opens the HTTP connection in synchronous mode.</span></span> <span data-ttu-id="cd3ae-119">Una chiamata a [**Send**](iwinhttprequest-send.md) non restituisce fino a quando [WinHTTP](about-winhttp.md) non ha ricevuto completamente la risposta.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-119">A call to [**Send**](iwinhttprequest-send.md) does not return until [WinHTTP](about-winhttp.md) has completely received the response.</span></span><br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="cd3ae-120"><dt>**VARIANT \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="cd3ae-120"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="cd3ae-121">Apre la connessione HTTP in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-121">Opens the HTTP connection in asynchronous mode.</span></span><br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd3ae-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd3ae-122">Return value</span></span>

<span data-ttu-id="cd3ae-123">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd3ae-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd3ae-124">Remarks</span></span>

<span data-ttu-id="cd3ae-125">Questo metodo apre una connessione alla risorsa identificata nell' *URL* usando il [*verbo http*](glossary.md) specificato nel *Metodo*.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-125">This method opens a connection to the resource identified in *Url* using the [*HTTP verb*](glossary.md) given in *Method*.</span></span>

> [!Note]  
> <span data-ttu-id="cd3ae-126">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-126">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cd3ae-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="cd3ae-127">Examples</span></span>

<span data-ttu-id="cd3ae-128">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-128">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print the response to a console.
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



<span data-ttu-id="cd3ae-129">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-129">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cd3ae-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd3ae-130">Requirements</span></span>



| <span data-ttu-id="cd3ae-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd3ae-131">Requirement</span></span> | <span data-ttu-id="cd3ae-132">Valore</span><span class="sxs-lookup"><span data-stu-id="cd3ae-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3ae-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd3ae-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3ae-134">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="cd3ae-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="cd3ae-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd3ae-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3ae-136">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="cd3ae-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="cd3ae-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cd3ae-137">Redistributable</span></span><br/>          | <span data-ttu-id="cd3ae-138">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cd3ae-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="cd3ae-139">IDL</span><span class="sxs-lookup"><span data-stu-id="cd3ae-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd3ae-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd3ae-140"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="cd3ae-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd3ae-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd3ae-142"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd3ae-142"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="cd3ae-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cd3ae-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd3ae-144"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd3ae-144"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cd3ae-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd3ae-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3ae-146">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="cd3ae-146">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="cd3ae-147">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="cd3ae-147">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="cd3ae-148">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="cd3ae-148">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




