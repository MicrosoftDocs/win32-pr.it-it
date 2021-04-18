---
description: Fornisce eventi per i servizi HTTP di Microsoft Windows (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interfaccia IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317004"
---
# <a name="iwinhttprequestevents-interface"></a>Interfaccia IWinHttpRequestEvents

L'interfaccia **IWinHttpRequestEvents** fornisce eventi per i [Servizi http di Microsoft Windows (WinHTTP)](about-winhttp.md). USA solo metodi di evento.

## <a name="members"></a>Membri

L'interfaccia **IWinHttpRequestEvents** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequestEvents** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWinHttpRequestEvents** dispone di questi metodi.



| Metodo                                                                           | Descrizione                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Si verifica in presenza di un errore di run-time nell'applicazione.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Si verifica quando i dati sono disponibili dalla risposta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Si verifica quando i dati della risposta sono completi.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Si verifica quando i dati di risposta iniziano a essere ricevuti.<br/>      |



 

## <a name="remarks"></a>Commenti

Nella procedura riportata di seguito viene descritto come eseguire la registrazione per le notifiche.

1.  Ottenere un'interfaccia [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) chiamando **QueryInterface** su un oggetto [**IWinHttpRequest**](iwinhttprequest-interface.md) .
2.  Chiamare [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) sull'interfaccia restituita e passare **IID \_ IWinHttpRequestEvents** a *riid*.
3.  Chiamare [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) sul punto di connessione restituito e passare un puntatore a un'interfaccia **IUnknown** su un oggetto che implementa **IWinHttpRequestEvents** in *punk*.

È possibile terminare le notifiche chiamando [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) sul punto di connessione restituito nel passaggio 2.

Per visualizzare il codice che registra per le notifiche COM, vedere la sezione client dell'articolo [punti di connessione com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

