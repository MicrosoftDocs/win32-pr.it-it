---
description: Il metodo setimeouts specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: 'Metodo IWinHttpRequest:: setimeouts'
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
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234919"
---
# <a name="iwinhttprequestsettimeouts-method"></a>Metodo IWinHttpRequest:: setimeouts

Il metodo **Setimeouts** specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.

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

*ResolveTimeout* \[ in\]
</dt> <dd>

Valore di timeout applicato durante la risoluzione di un nome host (ad esempio `www.microsoft.com` ) in un indirizzo IP (ad esempio 192.168.131.199), in millisecondi. Il valore predefinito è zero, ovvero nessun timeout (infinito). Se il timeout DNS viene specificato con \_ il \_ timeout di risoluzione dei nomi, si verifica un sovraccarico di un thread per ogni richiesta.

</dd> <dt>

*ConnectTimeout* \[ in\]
</dt> <dd>

Valore di timeout applicato quando si stabilisce un socket di comunicazione con il server di destinazione, in millisecondi. Il valore predefinito è 60.000 (60 secondi).

</dd> <dt>

*SendTimeout nell'elemento* \[ in\]
</dt> <dd>

Valore di timeout applicato quando si invia un singolo pacchetto di dati di richiesta sul socket di comunicazione al server di destinazione, in millisecondi. Una richiesta di grandi dimensioni inviata a un server HTTP in genere viene suddivisa in più pacchetti; il timeout di invio si applica all'invio di ogni pacchetto singolarmente. Il valore predefinito è 30.000 (30 secondi).

</dd> <dt>

*ReceiveTimeout* \[ in\]
</dt> <dd>

Valore di timeout applicato durante la ricezione di un pacchetto di dati di risposta dal server di destinazione, in millisecondi. Le risposte di grandi dimensioni vengono suddivise in più pacchetti; il timeout di ricezione si applica al recupero di ogni pacchetto di dati dal socket. Il valore predefinito è 30.000 (30 secondi).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Tutti i parametri sono obbligatori. Un valore pari a 0 o-1 imposta un timeout per un'attesa infinita. Un valore maggiore di 0 imposta il valore di timeout in millisecondi. 30.000, ad esempio, imposterà il timeout su 30 secondi. Tutti i valori negativi diversi da-1 determinano l'esito negativo di questo metodo.

I valori di timeout vengono applicati a livello di Winsock.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come impostare tutti i timeout di WinHTTP su 30 secondi, aprire una connessione HTTP, inviare una richiesta HTTP e leggere il testo della risposta.


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



Nell'esempio di script seguente viene illustrato come impostare tutti i timeout di WinHTTP su 30 secondi, aprire una connessione HTTP e inviare una richiesta HTTP.


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

 

 




