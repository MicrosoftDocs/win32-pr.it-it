---
Description: In questo argomento vengono fornite informazioni sull'utilizzo dell'oggetto COM WinHTTP WinHttpRequest con i linguaggi di scripting.
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
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328193"
---
# <a name="winhttprequest-object"></a>Oggetto WinHttpRequest

In questo argomento vengono fornite informazioni sull'utilizzo dell'oggetto com WinHTTP **WinHttpRequest** con i linguaggi di scripting. Per ulteriori informazioni, tra cui l'API C++ (WinHTTP), consultare [informazioni su WinHTTP](about-winhttp.md). Vedere [scelta di un'interfaccia WinHTTP](choosing-a-winhttp-interface.md) per un confronto di queste interfacce.

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

Esempi di codice ricavati dalla [Proprietà IWinHttpRequest:: status](iwinhttprequest-status.md).



## <a name="members"></a>Membri

L'oggetto **WinHttpRequest** dispone di questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

L'oggetto **WinHttpRequest** presenta questi eventi.



| Event                                                                            | Descrizione                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Si verifica in presenza di un errore di run-time nell'applicazione.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Si verifica quando i dati sono disponibili dalla risposta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Si verifica quando i dati della risposta sono completi.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Si verifica quando i dati di risposta iniziano a essere ricevuti.<br/>      |



 

### <a name="methods"></a>Metodi

L'oggetto **WinHttpRequest** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interruzione**](iwinhttprequest-abort.md)                                 | Interrompe un metodo di [**invio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera tutte le intestazioni di risposta HTTP.<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera le intestazioni della risposta HTTP.<br/>                                                                                                            |
| [**Aprire**](iwinhttprequest-open.md)                                   | Apre una connessione HTTP a una risorsa HTTP.<br/>                                                                                                   |
| [**Invia**](iwinhttprequest-send.md)                                   | Invia una richiesta HTTP a un server HTTP.<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Imposta i [criteri di accesso automatici](authentication-in-winhttp.md)correnti.<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Imposta le credenziali da utilizzare con un server HTTP, un'origine o un server proxy.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Imposta le informazioni sul server proxy.<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Aggiunge, modifica o Elimina un'intestazione della richiesta HTTP.<br/>                                                                                               |
| [**Timeout**](iwinhttprequest-settimeouts.md)                     | Specifica, in millisecondi, i singoli componenti di timeout di un'operazione di invio/ricezione.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Specifica il tempo di attesa, in secondi, per il completamento di un metodo di [**invio**](iwinhttprequest-send.md) asincrono, con un valore di timeout facoltativo.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **WinHttpRequest** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Opzione**](iwinhttprequest-option.md)<br/>                 | Lettura/Scrittura<br/> | Imposta o recupera un valore di opzione WinHTTP.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Sola lettura<br/>  | Recupera il corpo dell'entità della risposta come matrice di byte senza segno.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Sola lettura<br/>  | Recupera il corpo dell'entità di risposta come [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Sola lettura<br/>  | Recupera il corpo dell'entità di risposta come testo.<br/>                          |
| [**Stato**](iwinhttprequest-status.md)<br/>                 | Sola lettura<br/>  | Recupera il codice di stato HTTP dall'ultima risposta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Sola lettura<br/>  | Recupera il testo di stato HTTP.<br/>                                          |



 

## <a name="remarks"></a>Commenti

L'oggetto **WinHttpRequest** utilizza l'interfaccia [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) per fornire i dati di errore. È possibile ottenere una descrizione e un valore di errore numerico con l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) in Microsoft Visual Basic Scripting Edition (VBScript) e l'oggetto [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) in Microsoft JScript. I 16 bit inferiori di un numero di errore corrispondono ai valori trovati nei [**messaggi di errore**](error-messages.md).

> [!Note]  
> Per Windows XP e Windows 2000, vedere [requisiti di run-time](winhttp-start-page.md).

 

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

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

