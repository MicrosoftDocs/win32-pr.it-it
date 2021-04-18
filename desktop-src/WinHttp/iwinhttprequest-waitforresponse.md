---
description: Il metodo WaitForResponse attende il completamento di un metodo Send asincrono, con un valore di timeout facoltativo, in secondi.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: 'Metodo IWinHttpRequest:: WaitForResponse'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317005"
---
# <a name="iwinhttprequestwaitforresponse-method"></a>Metodo IWinHttpRequest:: WaitForResponse

Il metodo **waitForResponse** attende il completamento di un metodo [**Send**](iwinhttprequest-send.md) asincrono, con un valore di timeout facoltativo, in secondi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Timeout* \[ in, facoltativo\]
</dt> <dd>

Valore di timeout, in secondi. Il timeout predefinito è infinito. Per impostare in modo esplicito il timeout su infinito, utilizzare il valore-1.

</dd> <dt>

Operazione *riuscita* \[ out, retval\]
</dt> <dd>

Riceve uno dei valori seguenti.



| Valore                                                                                                                                                         | Significato                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**VARIANT \_ true**</dt> </dl>    | È stata ricevuta una risposta.<br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**VARIANTE \_ false**</dt> </dl> | È stato superato il periodo di timeout specificato.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Questo metodo sospende l'esecuzione in attesa di una risposta a una richiesta asincrona. Questo metodo deve essere chiamato dopo un'operazione [**Send**](iwinhttprequest-send.md). La chiamata di applicazioni può specificare un valore di *timeout* facoltativo, in secondi. Se si verifica il timeout di questo metodo, la richiesta non viene interrotta. In questo modo, l'applicazione chiamante può continuare ad attendere la richiesta, se necessario, in una chiamata successiva a questo metodo.

La chiamata di questa proprietà dopo un metodo di [**invio**](iwinhttprequest-send.md) sincrono viene restituita immediatamente e non ha alcun effetto.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come aprire una connessione HTTP asincrona, inviare una richiesta HTTP, attendere la risposta e leggere il testo della risposta.


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
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

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
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



Nell'esempio di script seguente viene illustrato come aprire una connessione HTTP asincrona, inviare una richiesta HTTP, attendere una risposta e leggere il testo della risposta.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

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

[**Aprire**](iwinhttprequest-open.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




