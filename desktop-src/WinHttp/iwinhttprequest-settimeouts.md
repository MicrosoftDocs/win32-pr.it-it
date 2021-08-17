---
description: Il metodo SetTimeouts specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: Metodo IWinHttpRequest::SetTimeouts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: e31fbe80f106735a43126b2be5181478b932e2f813b207984959cf013d3fd752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562456"
---
# <a name="iwinhttprequestsettimeouts-method"></a>Metodo IWinHttpRequest::SetTimeouts

Il **metodo SetTimeouts** specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ResolveTimeout* \[ Pollici\]
</dt> <dd>

Valore di timeout applicato durante la risoluzione di un nome host (ad esempio ) in un indirizzo IP (ad esempio `www.microsoft.com` 192.168.131.199), in millisecondi. Il valore predefinito è zero, ovvero nessun timeout (infinito). Se il timeout DNS viene specificato usando NAME \_ RESOLUTION \_ TIMEOUT, si verifica un sovraccarico di un thread per ogni richiesta.

</dd> <dt>

*ConnectTimeout* \[ Pollici\]
</dt> <dd>

Valore di timeout applicato quando si stabilisce un socket di comunicazione con il server di destinazione, in millisecondi. Il valore predefinito è 60.000 (60 secondi).

</dd> <dt>

*SendTimeout* \[ Pollici\]
</dt> <dd>

Valore di timeout applicato durante l'invio di un singolo pacchetto di dati della richiesta sul socket di comunicazione al server di destinazione, in millisecondi. Una richiesta di grandi dimensioni inviata a un server HTTP viene in genere suddivisa in più pacchetti. Il timeout di invio si applica all'invio di ogni pacchetto singolarmente. Il valore predefinito è 30.000 (30 secondi).

</dd> <dt>

*ReceiveTimeout* \[ Pollici\]
</dt> <dd>

Valore di timeout applicato quando si riceve un pacchetto di dati di risposta dal server di destinazione, in millisecondi. Le risposte di grandi dimensioni sono suddivise in più pacchetti. Il timeout di ricezione si applica al recupero di ogni pacchetto di dati dal socket. Il valore predefinito è 30.000 (30 secondi).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **S \_ OK in caso** di esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Tutti i parametri sono obbligatori. Il valore 0 o -1 imposta un timeout per l'attesa infinita. Un valore maggiore di 0 imposta il valore di timeout in millisecondi. Ad esempio, 30.000 impostano il timeout su 30 secondi. Tutti i valori negativi diversi da -1 causano l'esito negativo di questo metodo.

I valori di timeout vengono applicati al livello Winsock.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHttp.

 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come impostare tutti i timeout WinHTTP su 30 secondi, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.


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
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
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



L'esempio di scripting seguente mostra come impostare tutti i timeout WinHTTP su 30 secondi, aprire una connessione HTTP e inviare una richiesta HTTP.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send();
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

 

 




