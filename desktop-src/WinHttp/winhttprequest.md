---
Description: Questo argomento fornisce informazioni sull'uso dell'oggetto COM WinHTTP WinHttpRequest con linguaggi di scripting.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Oggetto WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 92fdcb9c6eff502dc5f19cb62d92af5d4db60e15890667c894f96cfb55a9e5ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132914"
---
# <a name="winhttprequest-object"></a>Oggetto WinHttpRequest

Questo argomento fornisce informazioni sull'uso dell'oggetto COM **WinHTTP WinHttpRequest** con linguaggi di scripting. Per altre informazioni, inclusa l'API C++ (WinHTTP), vedere [Informazioni su WinHTTP.](about-winhttp.md) Per un confronto di queste interfacce, vedere Scelta di un'interfaccia [WinHTTP.](choosing-a-winhttp-interface.md)

## <a name="example"></a>Esempio

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

Esempi di codice presi dalla [proprietà IWinHttpRequest::Status](iwinhttprequest-status.md).



## <a name="members"></a>Membri

**L'oggetto WinHttpRequest** ha questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

**L'oggetto WinHttpRequest** include questi eventi.



| Event                                                                            | Descrizione                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Si verifica quando si verifica un errore di run-time nell'applicazione.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Si verifica quando i dati sono disponibili dalla risposta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Si verifica quando i dati della risposta sono completi.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Si verifica quando i dati della risposta iniziano a essere ricevuti.<br/>      |



 

### <a name="methods"></a>Metodi

**L'oggetto WinHttpRequest** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interrompere**](iwinhttprequest-abort.md)                                 | Interrompe un [metodo WinHTTP](about-winhttp.md) [**Send.**](iwinhttprequest-send.md)<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera tutte le intestazioni di risposta HTTP.<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera le intestazioni della risposta HTTP.<br/>                                                                                                            |
| [**Aperto**](iwinhttprequest-open.md)                                   | Apre una connessione HTTP a una risorsa HTTP.<br/>                                                                                                   |
| [**Invia**](iwinhttprequest-send.md)                                   | Invia una richiesta HTTP a un server HTTP.<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Imposta i criteri [di accesso automatico correnti.](authentication-in-winhttp.md)<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Imposta le credenziali da utilizzare con un server HTTP di origine o proxy.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Imposta le informazioni sul server proxy.<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Aggiunge, modifica o elimina un'intestazione di richiesta HTTP.<br/>                                                                                               |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Specifica, in millisecondi, i singoli componenti di timeout di un'operazione di invio/ricezione.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Specifica il tempo di attesa, in secondi, per il completamento di un metodo [**Send**](iwinhttprequest-send.md) asincrono, con valore di timeout facoltativo.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto WinHttpRequest** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Opzione**](iwinhttprequest-option.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o recupera un valore dell'opzione WinHTTP.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Sola lettura<br/>  | Recupera il corpo dell'entità di risposta come matrice di byte senza segno.<br/>    |
| [**Responsestream**](iwinhttprequest-responsestream.md)<br/> | Sola lettura<br/>  | Recupera il corpo dell'entità di risposta come [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Sola lettura<br/>  | Recupera il corpo dell'entità di risposta come testo.<br/>                          |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Sola lettura<br/>  | Recupera il codice di stato HTTP dall'ultima risposta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Sola lettura<br/>  | Recupera il testo dello stato HTTP.<br/>                                          |



 

## <a name="remarks"></a>Commenti

**L'oggetto WinHttpRequest** usa [**l'interfaccia IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) per fornire i dati degli errori. È possibile ottenere una descrizione e un valore di errore numerico con l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) in Microsoft Visual Basic Scripting Edition (VBScript) e l'oggetto [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) in Microsoft JScript. I 16 bit inferiori di un numero di errore corrispondono ai valori trovati in [**Messaggi di errore**](error-messages.md).

> [!Note]  
> Per Windows XP e Windows 2000, vedere [Requisiti di run-time](winhttp-start-page.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

