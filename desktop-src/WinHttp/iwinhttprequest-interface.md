---
description: L'interfaccia IWinHttpRequest fornisce tutti i metodi non uniformi per i servizi HTTP di Microsoft Windows (WinHTTP).
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
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231832"
---
# <a name="iwinhttprequest-interface"></a>Interfaccia IWinHttpRequest

L'interfaccia **IWinHttpRequest** fornisce tutti i metodi non uniformi per i [Servizi http di Microsoft Windows (WinHTTP)](about-winhttp.md).

## <a name="members"></a>Membri

L'interfaccia **IWinHttpRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequest** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWinHttpRequest** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Interruzione**](iwinhttprequest-abort.md)                                 | Interrompe un metodo di [**invio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera tutte le intestazioni di risposta HTTP.<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera le intestazioni della risposta HTTP.<br/>                                                                                         |
| [**Aprire**](iwinhttprequest-open.md)                                   | Apre una connessione HTTP a una risorsa HTTP.<br/>                                                                                |
| [**Invia**](iwinhttprequest-send.md)                                   | Invia una richiesta HTTP a un server HTTP.<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Imposta i [criteri di accesso automatici](authentication-in-winhttp.md)correnti.<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Imposta le credenziali da utilizzare con un server HTTP, un server proxy o un server di origine.<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Imposta le informazioni sul server proxy.<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Aggiunge, modifica o Elimina un'intestazione della richiesta HTTP.<br/>                                                                            |
| [**Timeout**](iwinhttprequest-settimeouts.md)                     | Specifica i singoli componenti di timeout di un'operazione di invio/ricezione, in millisecondi.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Attende il completamento di un metodo di [**invio**](iwinhttprequest-send.md) asincrono, con un valore di timeout facoltativo, in secondi.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWinHttpRequest** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Opzione**](iwinhttprequest-option.md)<br/>                 | Lettura/Scrittura<br/> | Valore di opzione WinHTTP.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Sola lettura<br/>  | Corpo dell'entità della risposta come matrice di byte senza segno.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Sola lettura<br/>  | Corpo dell'entità della risposta come [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Sola lettura<br/>  | Corpo dell'entità della risposta.<br/>                                  |
| [**Stato**](iwinhttprequest-status.md)<br/>                 | Sola lettura<br/>  | Codice di stato HTTP dell'ultima risposta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Sola lettura<br/>  | Testo di stato HTTP.<br/>                                      |



 

## <a name="remarks"></a>Commenti

L'interfaccia **IWinHttpRequest** definita in HttpRequest. idl è implementata da una classe con ID **CLSID \_ WinHttpRequest**. Un'applicazione ottiene questa interfaccia chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un ID di classe **CLSID \_ WinHttpRequest** e un ID di interfaccia **IID \_ IWinHttpRequest**.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

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

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

