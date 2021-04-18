---
description: Si verifica quando i dati di risposta iniziano a essere ricevuti.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Evento IWinHttpRequestEvents:: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314105"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>Evento IWinHttpRequestEvents:: OnResponseStart

L'evento **OnResponseStart** si verifica quando i dati di risposta iniziano a essere ricevuti.

## <a name="syntax"></a>Sintassi


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato* \[ di in\]
</dt> <dd>

Riceve il codice di stato standard restituito con i dati di risposta. I codici di stato sono definiti nella [specifica RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

*ContentType* \[ in\]
</dt> <dd>

Specifica il tipo di contenuto ricevuto, ad esempio "text/html" o "image/gif".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Per questo evento, utilizzare [**Open**](iwinhttprequest-open.md) per inviare una connessione HTTP in modalità asincrona e utilizzare [**Send**](iwinhttprequest-send.md) per inviare una richiesta di dati a un server Internet.

Questo è il primo evento WinHTTP che si verifica dopo l' [**invio**](iwinhttprequest-send.md).

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

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




