---
description: Il metodo Abort interrompe un metodo WinHTTP Send.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: Metodo IWinHttpRequest::Abort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ca70917139059e8b0d038797ad61b137a259d615f6098a52bc86466f8054c7b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071771"
---
# <a name="iwinhttprequestabort-method"></a>Metodo IWinHttpRequest::Abort

Il **metodo Abort** interrompe un metodo [WinHTTP](about-winhttp.md) [**Send.**](iwinhttprequest-send.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Abort();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il valore restituito è **S \_ OK in** caso di esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

È possibile interrompere metodi Send [](iwinhttprequest-send.md) asincroni e sincroni. Per interrompere un metodo [**Send**](iwinhttprequest-send.md) sincrono, è necessario chiamare **Abort** dall'interno di un [**evento IWinHttpRequestEvents.**](iwinhttprequestevents-interface.md)

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [Requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHttp.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 o versioni successive in Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




