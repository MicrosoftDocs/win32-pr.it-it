---
description: Si verifica quando i dati sono disponibili dalla risposta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Evento IWinHttpRequestEvents:: OnResponseDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314110"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Evento IWinHttpRequestEvents:: OnResponseDataAvailable

L'evento **OnResponseDataAvailable** si verifica quando i dati sono disponibili dalla risposta.

## <a name="syntax"></a>Sintassi


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dati* \[ di in\]
</dt> <dd>

Matrice di byte in base zero che riceve i dati di risposta ricevuti dai servizi HTTP di Microsoft Windows (WinHTTP) fino al momento in cui si verifica questo evento. Si tratta di una **variante** di tipo VT \_ array \| VT \_ Ui1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Poiché i dati sono in byte, devono essere convertiti in caratteri wide se inseriti in una stringa di caratteri wide (Unicode).

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

 

 




