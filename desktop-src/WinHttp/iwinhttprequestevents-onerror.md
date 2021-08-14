---
description: Si verifica quando si verifica un errore di run-time nell'applicazione.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: Evento IWinHttpRequestEvents::OnError
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31127dcc3155b804bbda1c3ab94ee8a410c73f5a96c3ecfc6f787479ccd51539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744339"
---
# <a name="iwinhttprequesteventsonerror-event"></a>Evento IWinHttpRequestEvents::OnError

**L'evento OnError** si verifica quando si verifica un errore di run-time nell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ErrorNumber* \[ Pollici\]
</dt> <dd>

Riceve il valore numerico dell'errore. I 16 bit inferiori di questo numero di errore corrispondono a uno degli errori elencati in [**Messaggi di errore**](error-messages.md).

</dd> <dt>

*ErrorDescription* \[ Pollici\]
</dt> <dd>

Specifica una breve descrizione dell'errore che si è verificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per Windows XP e Windows 2000, vedere la [sezione Requisiti di run-time](winhttp-start-page.md) della pagina iniziale WinHTTP.

 

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

 

 




