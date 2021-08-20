---
description: Si verifica quando i dati sono disponibili dalla risposta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: Evento IWinHttpRequestEvents::OnResponseDataAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b55f87584164a47b47920caf961f02f0bd9cc6596c4c90f76f381027af545e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114245"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Evento IWinHttpRequestEvents::OnResponseDataAvailable

**L'evento OnResponseDataAvailable** si verifica quando i dati sono disponibili dalla risposta.

## <a name="syntax"></a>Sintassi


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dati* \[ Pollici\]
</dt> <dd>

Matrice in base zero di byte che riceve i dati di risposta ricevuti da Microsoft Windows HTTP Services (WinHTTP) fino al momento in cui si verifica questo evento. Si tratta di **una VARIANTE** di tipo VT \_ ARRAY \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

Poiché i dati sono in byte, devono essere convertiti in caratteri wide se inseriti in una stringa di caratteri wide (Unicode).

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]<br/>         |
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

 

 




