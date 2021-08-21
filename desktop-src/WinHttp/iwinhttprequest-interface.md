---
description: L'interfaccia IWinHttpRequest fornisce tutti i metodi non evento per Microsoft Windows HTTP Services (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interfaccia IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 87a31ebe116726d70eb847fe54d563be57477f7133147226657c4c74135defa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114400"
---
# <a name="iwinhttprequest-interface"></a>Interfaccia IWinHttpRequest

**L'interfaccia IWinHttpRequest** fornisce tutti i metodi non evento per [Microsoft Windows HTTP Services (WinHTTP).](about-winhttp.md)

## <a name="members"></a>Membri

**L'interfaccia IWinHttpRequest** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWinHttpRequest** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IWinHttpRequest** include questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Interrompere**](iwinhttprequest-abort.md)                                 | Interrompe un [metodo Send WinHTTP.](about-winhttp.md) [](iwinhttprequest-send.md)<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera tutte le intestazioni di risposta HTTP.<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera le intestazioni di risposta HTTP.<br/>                                                                                         |
| [**Aperto**](iwinhttprequest-open.md)                                   | Apre una connessione HTTP a una risorsa HTTP.<br/>                                                                                |
| [**Invia**](iwinhttprequest-send.md)                                   | Invia una richiesta HTTP a un server HTTP.<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Imposta il criterio [di accesso automatico corrente.](authentication-in-winhttp.md)<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Imposta le credenziali da utilizzare con un server HTTP, un server proxy o un server di origine.<br/>                             |
| [**Proxy di impostazione**](iwinhttprequest-setproxy.md)                           | Imposta le informazioni sul server proxy.<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Aggiunge, modifica o elimina un'intestazione di richiesta HTTP.<br/>                                                                            |
| [**SetTimeouts**](iwinhttprequest-settimeouts.md)                     | Specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Attende il completamento di un [**metodo Send**](iwinhttprequest-send.md) asincrono, con valore di timeout facoltativo, espresso in secondi.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IWinHttpRequest** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Opzione**](iwinhttprequest-option.md)<br/>                 | Lettura/Scrittura<br/> | Valore dell'opzione WinHTTP.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Sola lettura<br/>  | Corpo dell'entità di risposta come matrice di byte senza segno.<br/>    |
| [**Responsestream**](iwinhttprequest-responsestream.md)<br/> | Sola lettura<br/>  | Corpo dell'entità di risposta come [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Sola lettura<br/>  | Corpo dell'entità di risposta.<br/>                                  |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Sola lettura<br/>  | Codice di stato HTTP dell'ultima risposta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Sola lettura<br/>  | Testo dello stato HTTP.<br/>                                      |



 

## <a name="remarks"></a>Commenti

**L'interfaccia IWinHttpRequest** definita in httprequest.idl viene implementata da una classe con ID **CLSID \_ WinHttpRequest.** Un'applicazione ottiene questa interfaccia chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con l'ID di classe **CLSID \_ WinHttpRequest** e l'ID di interfaccia **\_ IID IWinHttpRequest.**

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHttp.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

