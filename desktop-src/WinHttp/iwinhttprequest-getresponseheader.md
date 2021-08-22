---
description: Recupera le intestazioni di risposta HTTP.
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: Metodo IWinHttpRequest::GetResponseHeader
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
ms.openlocfilehash: 1566ea05f78f9e90a97db3a14c61f7c59cfc61ecdb1eb390823d99a32d4983ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643881"
---
# <a name="iwinhttprequestgetresponseheader-method"></a>Metodo IWinHttpRequest::GetResponseHeader

Il **metodo GetResponseHeader** recupera le intestazioni della risposta HTTP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Intestazione* \[ Pollici\]
</dt> <dd>

Specifica il nome dell'intestazione senza distinzione tra maiuscole e minuscole.

</dd> <dt>

*Valore* \[ out, retval\]
</dt> <dd>

Riceve le informazioni di intestazione risultanti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **S \_ OK in caso** di esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo restituisce il valore dell'intestazione della risposta denominata in *Header*. Tenere presente che i client di automazione, ad esempio lo script, ottengono i dati di intestazione come valore restituito dalla chiamata di funzione, non tramite un parametro di funzione. Richiamare questo metodo solo dopo che [**è stato**](iwinhttprequest-send.md) chiamato il metodo Send.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHTTP.

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere l'intestazione della data dalla risposta. Questo esempio deve essere eseguito da un prompt dei comandi.


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



L'esempio di scripting seguente illustra come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere l'intestazione della data dalla risposta.


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

[**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




