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
# <a name="iwinhttprequestsetrequestheader-method"></a>Metodo IWinHttpRequest:: SetRequestHeader

Il metodo **setRequestHeader** aggiunge, modifica o Elimina un'intestazione della richiesta HTTP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Intestazione* \[ di in\]
</dt> <dd>

Specifica il nome dell'intestazione da impostare, ad esempio "Depth". Questo parametro non deve contenere i due punti e deve essere il testo effettivo dell'intestazione HTTP.

</dd> <dt>

*Valore* \[ di in\]
</dt> <dd>

Specifica il valore dell'intestazione, ad esempio "Infinity".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Le intestazioni vengono trasferite tra reindirizzamenti. Questo può creare una vulnerabilità di sicurezza. Per evitare che vengano trasferiti intestazioni se si verifica un reindirizzamento, usare il callback [*\_ dello \_ stato WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) per correggere le intestazioni specifiche quando si verifica un reindirizzamento.

Il metodo **setRequestHeader** consente all'applicazione chiamante di aggiungere o eliminare un'intestazione di richiesta HTTP prima di inviare la richiesta. Il nome dell'intestazione viene specificato nell' *intestazione* e il valore o il token di intestazione viene specificato in *valore*. Per aggiungere un'intestazione, fornire un nome e un valore di intestazione. Se esiste già un'altra intestazione con questo nome, questa viene sostituita. Per eliminare un'intestazione, impostare l' *intestazione* sul nome dell'intestazione da eliminare e impostare il *valore* su **null**.

Il nome e il valore delle intestazioni della richiesta aggiunti con questo metodo vengono convalidati. Le intestazioni devono essere ben formate. Per ulteriori informazioni sulle intestazioni HTTP valide, vedere [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Se viene utilizzata un'intestazione non valida, si verifica un errore e l'intestazione non viene aggiunta.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come aprire una connessione HTTP, impostare un'intestazione di richiesta, inviare una richiesta HTTP e leggere il testo della risposta. Questo esempio deve essere eseguito da un prompt dei comandi.


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



Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP, impostare un'intestazione di richiesta e inviare una richiesta HTTP.


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

 

