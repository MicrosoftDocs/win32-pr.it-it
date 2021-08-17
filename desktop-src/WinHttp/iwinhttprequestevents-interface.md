---
description: Fornisce eventi per i servizi HTTP Windows Microsoft (WinHTTP).
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
ms.openlocfilehash: 42b8355de57ada064e57a129c77ba507a72028b1c38ce115e58db110f2ce976b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744349"
---
# <a name="iwinhttprequestevents-interface"></a>Interfaccia IWinHttpRequestEvents

**L'interfaccia IWinHttpRequestEvents** fornisce eventi per [i servizi HTTP di Microsoft Windows (WinHTTP).](about-winhttp.md) Usa solo metodi di evento.

## <a name="members"></a>Membri

**L'interfaccia IWinHttpRequestEvents** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWinHttpRequestEvents** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWinHttpRequestEvents.**



| Metodo                                                                           | Descrizione                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Si verifica quando si verifica un errore di run-time nell'applicazione.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Si verifica quando i dati sono disponibili dalla risposta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Si verifica quando i dati della risposta sono completi.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Si verifica quando i dati della risposta iniziano a essere ricevuti.<br/>      |



 

## <a name="remarks"></a>Commenti

La procedura seguente descrive come eseguire la registrazione per le notifiche.

1.  Ottenere [un'interfaccia IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) chiamando **QueryInterface** su un [**oggetto IWinHttpRequest.**](iwinhttprequest-interface.md)
2.  Chiamare [FindConnectionPoint sull'interfaccia](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) restituita e passare **\_ IID IWinHttpRequestEvents** a *riid*.
3.  Chiamare [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) sul punto di connessione restituito e passare un puntatore a **un'interfaccia IUnknown** su un oggetto che implementa **IWinHttpRequestEvents** a *pUnk*.

Le notifiche possono essere terminate chiamando [Unadvise sul](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) punto di connessione restituito nel passaggio 2.

Per visualizzare il codice registrato per le notifiche COM, vedere la sezione Client [dell'articolo Punti di connessione COM.](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points)

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

