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
# <a name="iwinhttprequestsetproxy-method"></a>Metodo IWinHttpRequest:: seproxy

Il metodo **seproxy** imposta le informazioni sul server proxy.

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

*ProxySetting* \[ in\]
</dt> <dd>

Flag che controllano questo metodo. Può essere uno dei valori seguenti.



| Valore                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>\_ \_ impostazione predefinita HTTPREQUEST PROXYSETTING</dt> </dl>   | Impostazione predefinita del proxy. Equivalente a **HTTPREQUEST \_ PROXYSETTING \_ preconfig**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>preconfigurazione di HTTPREQUEST \_ PROXYSETTING \_</dt> </dl> | Indica che le impostazioni proxy devono essere ottenute dal registro di sistema. Si presuppone che [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) sia stato eseguito. Se Proxycfg.exe non è stato eseguito e viene specificato **HttpRequest \_ PROXYSETTING \_ preconfig** , il comportamento è equivalente a **HttpRequest \_ PROXYSETTING \_ Direct**.<br/> |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ Direct</dt> </dl>    | Indica che è necessario accedere direttamente a tutti i server HTTP e HTTPS. Usare questo comando se non è presente alcun server proxy.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>\_proxy PROXYSETTING \_ HTTPREQUEST</dt> </dl>     | Quando si specifica il **\_ \_ proxy HTTPREQUEST PROXYSETTING** , *varProxyServer* deve essere impostato su una stringa del server proxy e *varBypassList* deve essere impostato su una stringa di elenco di bypass di dominio. Questa configurazione proxy si applica solo all'istanza corrente dell'oggetto [**WinHttpRequest**](winhttprequest.md) .<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[ in, facoltativo\]
</dt> <dd>

Impostare su una stringa del server proxy quando *ProxySetting* è uguale a **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> <dt>

Sottopaginazione *ignorata* \[ in, facoltativo\]
</dt> <dd>

Impostare su una stringa di elenco di bypass del dominio quando *ProxySetting* è uguale a **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Consente all'applicazione chiamante di specificare l'utilizzo di informazioni proxy predefinite (configurate dallo strumento di configurazione del proxy) o di eseguire l'override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md). Questo metodo deve essere chiamato prima di chiamare il metodo [**Send**](iwinhttprequest-send.md) . Se questo metodo viene chiamato dopo il metodo [**Send**](iwinhttprequest-send.md) , non ha alcun effetto.

[**IWinHttpRequest**](iwinhttprequest-interface.md) passa questi parametri ai servizi HTTP di Microsoft Windows (WinHTTP).

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare le impostazioni proxy per un server proxy specifico, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta. Questo esempio deve essere eseguito da un prompt dei comandi. Queste impostazioni proxy funzionano solo se si dispone di un server proxy denominato " \_ server proxy" che utilizza la porta 80 e se il computer è in grado di ignorare il server proxy quando il nome host termina con ". Microsoft.com".


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



Nell'esempio di script seguente viene illustrato come impostare le impostazioni proxy per un server proxy specifico, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta. Queste impostazioni proxy funzionano solo se si dispone di un server proxy denominato " \_ server proxy" che utilizza la porta 80 e se il computer è in grado di ignorare il server proxy quando il nome host termina con ". Microsoft.com".


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
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




