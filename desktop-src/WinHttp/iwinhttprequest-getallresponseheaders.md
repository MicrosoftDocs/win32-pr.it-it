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
# <a name="iwinhttprequestgetallresponseheaders-method"></a>Metodo IWinHttpRequest:: GetAllResponseHeaders

Il metodo **GetAllResponseHeaders** recupera tutte le intestazioni di risposta http.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Intestazioni* \[ di out, retval\]
</dt> <dd>

Riceve le informazioni di intestazione risultanti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Questo metodo restituisce tutte le intestazioni contenute nella risposta server più recente. Le singole intestazioni sono delimitate da una combinazione di ritorno a capo e avanzamento riga (ASCII 13 e 10). L'ultima voce è seguita da due delimitatori (13, 10, 13, 10). Richiamare questo metodo solo dopo la chiamata del metodo [**Send**](iwinhttprequest-send.md) .

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere tutte le intestazioni dalla risposta. Questo esempio deve essere eseguito da un prompt dei comandi.


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



Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, inviare una richiesta HTTP e ottenere tutte le intestazioni dalla risposta.


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

[**GetResponseHeader**](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




