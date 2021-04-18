---
description: Si verifica quando i dati della risposta sono completi.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Evento IWinHttpRequestEvents:: OnResponseFinished'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314108"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a>Evento IWinHttpRequestEvents:: OnResponseFinished

L'evento **OnResponseFinished** si verifica quando i dati di risposta sono completi.

## <a name="syntax"></a>Sintassi


```C++
void OnResponseFinished();
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo evento segnala che sono stati ricevuti tutti i dati di risposta relativi alla richiesta più recente. [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) non si ripete fino alla richiesta successiva.

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

 

 




