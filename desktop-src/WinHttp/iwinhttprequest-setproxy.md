---
description: Imposta le informazioni sul server proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: Metodo IWinHttpRequest::SetProxy
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
ms.openlocfilehash: bb85466da6b7492d04bd2e69f4cd51c0c390e9595df13af8d7e6768596771822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562596"
---
# <a name="iwinhttprequestsetproxy-method"></a>Metodo IWinHttpRequest::SetProxy

Il **metodo SetProxy** imposta le informazioni sul server proxy.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazione proxy* \[ Pollici\]
</dt> <dd>

Flag che controllano questo metodo. Può essere uno dei valori seguenti.



| Valore                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>IMPOSTAZIONE PROXY \_ HTTPREQUEST \_ PREDEFINITA</dt> </dl>   | Impostazione proxy predefinita. Equivale a **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG</dt> </dl> | Indica che le impostazioni del proxy devono essere ottenute dal Registro di sistema. In questo modo si [ presuppone cheProxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) sia stato eseguito. Se Proxycfg.exe non è stato eseguito ed è specificato **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG,** il comportamento è equivalente a **HTTPREQUEST \_ PROXYSETTING \_ DIRECT**.<br/> |
| <dl> <dt>PROXY \_ HTTPREQUESTSETTING \_ DIRETTO</dt> </dl>    | Indica che è necessario accedere direttamente a tutti i server HTTP e HTTPS. Usare questo comando se non è presente alcun server proxy.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ PROXY</dt> </dl>     | Quando **si specifica \_ HTTPREQUEST PROXYSETTING \_ PROXY,** *varProxyServer* deve essere impostato su una stringa del server proxy e *varBypassList* deve essere impostato su una stringa dell'elenco di bypass del dominio. Questa configurazione del proxy si applica solo all'istanza corrente [**dell'oggetto WinHttpRequest.**](winhttprequest.md)<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[ in, facoltativo\]
</dt> <dd>

Impostare su una stringa del server proxy quando *ProxySetting* è uguale a **HTTPREQUEST \_ PROXYSETTING \_ PROXY**.

</dd> <dt>

*BypassList* \[ in, facoltativo\]
</dt> <dd>

Impostare su una stringa dell'elenco di bypass del dominio quando *ProxySetting* è uguale a **HTTPREQUEST \_ PROXYSETTING \_ PROXY**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **S \_ OK in caso** di esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Consente all'applicazione chiamante di specificare l'uso di informazioni proxy predefinite (configurate dallo strumento di configurazione del proxy) o di eseguire l'override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md). Questo metodo deve essere chiamato prima di chiamare il [**metodo Send.**](iwinhttprequest-send.md) Se questo metodo viene chiamato dopo il [**metodo Send,**](iwinhttprequest-send.md) non ha alcun effetto.

[**IWinHttpRequest**](iwinhttprequest-interface.md) passa questi parametri a Microsoft Windows servizi HTTP (WinHTTP).

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare le impostazioni proxy per un server proxy specifico, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta. Questo esempio deve essere eseguito da un prompt dei comandi. Queste impostazioni proxy funzionano solo se si dispone di un server proxy denominato "server proxy" che usa la porta 80 e il computer può ignorare il server proxy quando il nome host termina con \_ ".microsoft.com".


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



L'esempio di scripting seguente illustra come impostare le impostazioni proxy per un server proxy specifico, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta. Queste impostazioni proxy funzionano solo se si dispone di un server proxy denominato "server proxy" che usa la porta 80 e il computer può ignorare il server proxy quando il nome host termina con \_ ".microsoft.com".


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




