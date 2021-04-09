---
description: Si verifica in presenza di un errore di run-time nell'applicazione.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Evento IWinHttpRequestEvents:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968443"
---
# <a name="iwinhttprequesteventsonerror-event"></a>Evento IWinHttpRequestEvents:: OnError

L'evento **OnError** si verifica in presenza di un errore di run-time nell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Numero errore* \[ in\]
</dt> <dd>

Riceve il valore numerico dell'errore. I 16 bit inferiori di questo numero di errore corrispondono a uno degli errori elencati nei [**messaggi di errore**](error-messages.md).

</dd> <dt>

*ErrorDescription* \[ in\]
</dt> <dd>

Specifica una breve descrizione dell'errore che si è verificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

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

 

 




