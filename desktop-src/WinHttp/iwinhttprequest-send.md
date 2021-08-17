---
description: Il metodo Send invia una richiesta HTTP a un server HTTP.
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: Metodo IWinHttpRequest::Send
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
ms.openlocfilehash: 47155c946d8f49655bf6336a858d2b0752c70caa80f9dd75e0f415ce18ea94c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562941"
---
# <a name="iwinhttprequestsend-method"></a>Metodo IWinHttpRequest::Send

Il **metodo Send** invia una richiesta HTTP a un server HTTP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Corpo* \[ in, facoltativo\]
</dt> <dd>

Dati da inviare al server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **S \_ OK in caso** di esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

La richiesta da inviare è stata definita in una chiamata precedente al [**metodo**](iwinhttprequest-open.md) Open. L'applicazione chiamante può fornire dati da inviare al server tramite il *parametro Body.* Se il [*verbo HTTP*](glossary.md) dell'oggetto [**Open**](iwinhttprequest-open.md) è "GET", questo metodo invia la richiesta senza *Body,* anche se viene fornito dall'applicazione chiamante.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHttp.

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.


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



L'esempio di scripting seguente illustra come aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.


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



Nell'esempio di scripting seguente viene illustrato come inviare dati a un server HTTP.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server solo con app desktop SP3 \[\]<br/>         |
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

 

 




