---
description: Imposta le informazioni sul server proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'Metodo IWinHttpRequest:: seproxy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319334"
---
# <a name="iwinhttprequestsetproxy-method"></a><span data-ttu-id="ca9cb-103">Metodo IWinHttpRequest:: seproxy</span><span class="sxs-lookup"><span data-stu-id="ca9cb-103">IWinHttpRequest::SetProxy method</span></span>

<span data-ttu-id="ca9cb-104">Il metodo **seproxy** imposta le informazioni sul server proxy.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-104">The **SetProxy** method sets proxy server information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca9cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca9cb-105">Syntax</span></span>


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a><span data-ttu-id="ca9cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca9cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca9cb-107">*ProxySetting* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca9cb-107">*ProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9cb-108">Flag che controllano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-108">The flags that control this method.</span></span> <span data-ttu-id="ca9cb-109">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-109">Can be one of the following values.</span></span>



| <span data-ttu-id="ca9cb-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ca9cb-110">Value</span></span>                                                                                                           | <span data-ttu-id="ca9cb-111">Significato</span><span class="sxs-lookup"><span data-stu-id="ca9cb-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca9cb-112"><dt>\_ \_ impostazione predefinita HTTPREQUEST PROXYSETTING</dt></span><span class="sxs-lookup"><span data-stu-id="ca9cb-112"><dt>HTTPREQUEST\_PROXYSETTING\_DEFAULT</dt></span></span> </dl>   | <span data-ttu-id="ca9cb-113">Impostazione predefinita del proxy.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-113">Default proxy setting.</span></span> <span data-ttu-id="ca9cb-114">Equivalente a **HTTPREQUEST \_ PROXYSETTING \_ preconfig**.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-114">Equivalent to **HTTPREQUEST\_PROXYSETTING\_PRECONFIG**.</span></span><br/>                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="ca9cb-115"><dt>preconfigurazione di HTTPREQUEST \_ PROXYSETTING \_</dt></span><span class="sxs-lookup"><span data-stu-id="ca9cb-115"><dt>HTTPREQUEST\_PROXYSETTING\_PRECONFIG</dt></span></span> </dl> | <span data-ttu-id="ca9cb-116">Indica che le impostazioni proxy devono essere ottenute dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-116">Indicates that the proxy settings should be obtained from the registry.</span></span> <span data-ttu-id="ca9cb-117">Si presuppone che [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) sia stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-117">This assumes that [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) has been run.</span></span> <span data-ttu-id="ca9cb-118">Se Proxycfg.exe non è stato eseguito e viene specificato **HttpRequest \_ PROXYSETTING \_ preconfig** , il comportamento è equivalente a **HttpRequest \_ PROXYSETTING \_ Direct**.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-118">If Proxycfg.exe has not been run and **HTTPREQUEST\_PROXYSETTING\_PRECONFIG** is specified, then the behavior is equivalent to **HTTPREQUEST\_PROXYSETTING\_DIRECT**.</span></span><br/> |
| <dl> <span data-ttu-id="ca9cb-119"><dt>HTTPREQUEST \_ PROXYSETTING \_ Direct</dt></span><span class="sxs-lookup"><span data-stu-id="ca9cb-119"><dt>HTTPREQUEST\_PROXYSETTING\_DIRECT</dt></span></span> </dl>    | <span data-ttu-id="ca9cb-120">Indica che è necessario accedere direttamente a tutti i server HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-120">Indicates that all HTTP and HTTPS servers should be accessed directly.</span></span> <span data-ttu-id="ca9cb-121">Usare questo comando se non è presente alcun server proxy.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-121">Use this command if there is no proxy server.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="ca9cb-122"><dt>\_proxy PROXYSETTING \_ HTTPREQUEST</dt></span><span class="sxs-lookup"><span data-stu-id="ca9cb-122"><dt>HTTPREQUEST\_PROXYSETTING\_PROXY</dt></span></span> </dl>     | <span data-ttu-id="ca9cb-123">Quando si specifica il **\_ \_ proxy HTTPREQUEST PROXYSETTING** , *varProxyServer* deve essere impostato su una stringa del server proxy e *varBypassList* deve essere impostato su una stringa di elenco di bypass di dominio.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-123">When **HTTPREQUEST\_PROXYSETTING\_PROXY** is specified, *varProxyServer* should be set to a proxy server string and *varBypassList* should be set to a domain bypass list string.</span></span> <span data-ttu-id="ca9cb-124">Questa configurazione proxy si applica solo all'istanza corrente dell'oggetto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="ca9cb-124">This proxy configuration applies only to the current instance of the [**WinHttpRequest**](winhttprequest.md) object.</span></span><br/>                                    |



 

</dd> <dt>

<span data-ttu-id="ca9cb-125">*ProxyServer* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca9cb-125">*ProxyServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9cb-126">Impostare su una stringa del server proxy quando *ProxySetting* è uguale a **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-126">Set to a proxy server string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> <dt>

<span data-ttu-id="ca9cb-127">Sottopaginazione *ignorata* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca9cb-127">*BypassList* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9cb-128">Impostare su una stringa di elenco di bypass del dominio quando *ProxySetting* è uguale a **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-128">Set to a domain bypass list string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca9cb-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca9cb-129">Return value</span></span>

<span data-ttu-id="ca9cb-130">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-130">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca9cb-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca9cb-131">Remarks</span></span>

<span data-ttu-id="ca9cb-132">Consente all'applicazione chiamante di specificare l'utilizzo di informazioni proxy predefinite (configurate dallo strumento di configurazione del proxy) o di eseguire l'override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="ca9cb-132">Enables the calling application to specify use of default proxy information (configured by the proxy configuration tool) or to override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span></span> <span data-ttu-id="ca9cb-133">Questo metodo deve essere chiamato prima di chiamare il metodo [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="ca9cb-133">This method must be called before calling the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="ca9cb-134">Se questo metodo viene chiamato dopo il metodo [**Send**](iwinhttprequest-send.md) , non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-134">If this method is called after the [**Send**](iwinhttprequest-send.md) method, it has no effect.</span></span>

<span data-ttu-id="ca9cb-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passa questi parametri ai servizi HTTP di Microsoft Windows (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="ca9cb-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passes these parameters to Microsoft Windows HTTP Services (WinHTTP).</span></span>

> [!Note]  
> <span data-ttu-id="ca9cb-136">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-136">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ca9cb-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="ca9cb-137">Examples</span></span>

<span data-ttu-id="ca9cb-138">Nell'esempio seguente viene illustrato come impostare le impostazioni proxy per un server proxy specifico, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-138">The following example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="ca9cb-139">Questo esempio deve essere eseguito da un prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-139">This example must be run from a command prompt.</span></span> <span data-ttu-id="ca9cb-140">Queste impostazioni proxy funzionano solo se si dispone di un server proxy denominato " \_ server proxy" che utilizza la porta 80 e se il computer è in grado di ignorare il server proxy quando il nome host termina con ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="ca9cb-140">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


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
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
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
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



<span data-ttu-id="ca9cb-141">Nell'esempio di script seguente viene illustrato come impostare le impostazioni proxy per un server proxy specifico, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-141">The following scripting example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="ca9cb-142">Queste impostazioni proxy funzionano solo se si dispone di un server proxy denominato " \_ server proxy" che utilizza la porta 80 e se il computer è in grado di ignorare il server proxy quando il nome host termina con ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="ca9cb-142">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="ca9cb-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca9cb-143">Requirements</span></span>



| <span data-ttu-id="ca9cb-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca9cb-144">Requirement</span></span> | <span data-ttu-id="ca9cb-145">Valore</span><span class="sxs-lookup"><span data-stu-id="ca9cb-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca9cb-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca9cb-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ca9cb-147">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="ca9cb-147">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="ca9cb-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca9cb-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ca9cb-149">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="ca9cb-149">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="ca9cb-150">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ca9cb-150">Redistributable</span></span><br/>          | <span data-ttu-id="ca9cb-151">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ca9cb-151">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="ca9cb-152">IDL</span><span class="sxs-lookup"><span data-stu-id="ca9cb-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca9cb-153"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca9cb-153"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="ca9cb-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca9cb-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca9cb-155"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca9cb-155"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="ca9cb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ca9cb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca9cb-157"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca9cb-157"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ca9cb-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca9cb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca9cb-159">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ca9cb-159">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="ca9cb-160">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ca9cb-160">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="ca9cb-161">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ca9cb-161">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




