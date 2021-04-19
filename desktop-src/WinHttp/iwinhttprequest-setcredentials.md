---
description: Imposta le credenziali da utilizzare con un server HTTP, indipendentemente dal fatto che si tratti di un server proxy o di un server di origine.
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: 'Metodo IWinHttpRequest:: secredentials'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 46b0dfb321763a3b3bfe622e116f2e76c5e59423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313696"
---
# <a name="iwinhttprequestsetcredentials-method"></a><span data-ttu-id="91c3b-103">Metodo IWinHttpRequest:: secredentials</span><span class="sxs-lookup"><span data-stu-id="91c3b-103">IWinHttpRequest::SetCredentials method</span></span>

<span data-ttu-id="91c3b-104">Il metodo **Secredentials** imposta le credenziali da utilizzare con un server http, indipendentemente dal fatto che si tratti di un server proxy o di un server di origine.</span><span class="sxs-lookup"><span data-stu-id="91c3b-104">The **SetCredentials** method sets credentials to be used with an HTTP server, whether it is a proxy server or an originating server.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91c3b-105">Syntax</span></span>


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="91c3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91c3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c3b-107">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c3b-107">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c3b-108">Specifica il nome utente per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="91c3b-108">Specifies the user name for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="91c3b-109">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="91c3b-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c3b-110">Specifica la password per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="91c3b-110">Specifies the password for authentication.</span></span> <span data-ttu-id="91c3b-111">Questo parametro viene ignorato se *bstrUserName* è **null** o mancante.</span><span class="sxs-lookup"><span data-stu-id="91c3b-111">This parameter is ignored if *bstrUserName* is **NULL** or missing.</span></span>

</dd> <dt>

<span data-ttu-id="91c3b-112">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91c3b-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c3b-113">Specifica quando [**IWinHttpRequest**](iwinhttprequest-interface.md) usa le credenziali.</span><span class="sxs-lookup"><span data-stu-id="91c3b-113">Specifies when [**IWinHttpRequest**](iwinhttprequest-interface.md) uses credentials.</span></span> <span data-ttu-id="91c3b-114">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="91c3b-114">Can be one of the following values.</span></span>



| <span data-ttu-id="91c3b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="91c3b-115">Value</span></span>                                                                                                               | <span data-ttu-id="91c3b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="91c3b-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="91c3b-117"><dt>\_credenziali HTTPREQUEST \_ per il \_ Server</dt></span><span class="sxs-lookup"><span data-stu-id="91c3b-117"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER</dt></span></span> </dl> | <span data-ttu-id="91c3b-118">Le credenziali vengono passate a un server.</span><span class="sxs-lookup"><span data-stu-id="91c3b-118">Credentials are passed to a server.</span></span><br/> |
| <dl> <span data-ttu-id="91c3b-119"><dt>\_credenziali HTTPREQUEST \_ per il \_ proxy</dt></span><span class="sxs-lookup"><span data-stu-id="91c3b-119"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY</dt></span></span> </dl>  | <span data-ttu-id="91c3b-120">Le credenziali vengono passate a un proxy.</span><span class="sxs-lookup"><span data-stu-id="91c3b-120">Credentials are passed to a proxy.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c3b-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91c3b-121">Return value</span></span>

<span data-ttu-id="91c3b-122">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="91c3b-122">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c3b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="91c3b-123">Remarks</span></span>

<span data-ttu-id="91c3b-124">Questo metodo restituisce un valore di errore se una chiamata a [**Open**](iwinhttprequest-open.md) non è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="91c3b-124">This method returns an error value if a call to [**Open**](iwinhttprequest-open.md) has not completed successfully.</span></span> <span data-ttu-id="91c3b-125">Si presuppone che una certa interazione con un server proxy o un server di origine debba verificarsi prima che gli utenti possano impostare le credenziali per la sessione.</span><span class="sxs-lookup"><span data-stu-id="91c3b-125">It is assumed that some measure of interaction with a proxy server or origin server must occur before users can set credentials for the session.</span></span> <span data-ttu-id="91c3b-126">Inoltre, fino a quando gli utenti non conoscono gli schemi di autenticazione supportati, non possono formattare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="91c3b-126">Moreover, until users know which authentication scheme(s) are supported, they cannot format the credentials.</span></span>

> [!Note]  
> <span data-ttu-id="91c3b-127">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="91c3b-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

<span data-ttu-id="91c3b-128">Per eseguire l'autenticazione con il server e il proxy, l'applicazione deve chiamare due volte le **credenziali** . innanzitutto con il parametro *Flags* impostato su **HttpRequest le \_ credenziali per il \_ \_ Server** e Second, con il parametro *Flags* impostato su **HttpRequest le \_ credenziali per il \_ \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="91c3b-128">To authenticate with both the server and the proxy, the application must call **SetCredentials** twice; first with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER**, and second, with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY**.</span></span>

## <a name="examples"></a><span data-ttu-id="91c3b-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="91c3b-129">Examples</span></span>

<span data-ttu-id="91c3b-130">Nell'esempio seguente viene illustrato come aprire una connessione HTTP, impostare le credenziali per il server, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="91c3b-130">The following example shows how to open an HTTP connection, set credentials for the server, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="91c3b-131">Questo esempio deve essere eseguito da un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="91c3b-131">This example must be run from a command prompt.</span></span>


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
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
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



<span data-ttu-id="91c3b-132">Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, impostare le credenziali per il server, impostare le credenziali per un proxy se ne viene usato uno, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="91c3b-132">The following scripting example shows how to open an HTTP connection, set credentials for the server, set credentials for a proxy if one is used, send an HTTP request, and read the response text.</span></span>


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="91c3b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91c3b-133">Requirements</span></span>



| <span data-ttu-id="91c3b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c3b-134">Requirement</span></span> | <span data-ttu-id="91c3b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="91c3b-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c3b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91c3b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="91c3b-137">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="91c3b-137">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="91c3b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91c3b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="91c3b-139">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="91c3b-139">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="91c3b-140">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="91c3b-140">Redistributable</span></span><br/>          | <span data-ttu-id="91c3b-141">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="91c3b-141">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="91c3b-142">IDL</span><span class="sxs-lookup"><span data-stu-id="91c3b-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91c3b-143"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91c3b-143"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="91c3b-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="91c3b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="91c3b-145"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91c3b-145"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="91c3b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="91c3b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91c3b-147"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c3b-147"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="91c3b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91c3b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c3b-149">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="91c3b-149">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="91c3b-150">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="91c3b-150">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="91c3b-151">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="91c3b-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




