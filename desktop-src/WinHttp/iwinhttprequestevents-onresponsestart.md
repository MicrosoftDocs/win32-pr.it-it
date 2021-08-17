---
description: Si verifica quando inizia la ricezione dei dati della risposta.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: Evento IWinHttpRequestEvents::OnResponseStart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb08273bfbab92e957b932f463ce4b91ee53e3663dcd886f5e02b73698fff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744224"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>Evento IWinHttpRequestEvents::OnResponseStart

**L'evento OnResponseStart** si verifica quando inizia la ricezione dei dati della risposta.

## <a name="syntax"></a>Sintassi


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato* \[ Pollici\]
</dt> <dd>

Riceve il codice di stato standard restituito con i dati della risposta. I codici di stato sono definiti in [RFC 2616.](https://www.ietf.org/rfc/rfc2616.txt)

</dd> <dt>

*ContentType* \[ Pollici\]
</dt> <dd>

Specifica il tipo di contenuto ricevuto, ad esempio "text/html" o "image/gif".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per questo evento, usare [**Open**](iwinhttprequest-open.md) per inviare una connessione HTTP in modalità asincrona e [**Send**](iwinhttprequest-send.md) per inviare una richiesta di dati a un server Internet.

Si tratta del primo evento WinHTTP che si verifica dopo [**l'invio di**](iwinhttprequest-send.md).

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHTTP.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server solo con app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




