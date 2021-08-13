---
description: Recupera il corpo dell'entità di risposta come matrice di byte senza segno.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: Proprietà IWinHttpRequest::ResponseBody
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56eac42d41054cf7c01ff0c69ffcb82353db7182acf15765b25149560d5f7391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563229"
---
# <a name="iwinhttprequestresponsebody-property"></a>Proprietà IWinHttpRequest::ResponseBody

La **proprietà ResponseBody** recupera il corpo dell'entità di risposta come matrice di byte senza segno.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a>Valore proprietà

Valore **Variant** che riceve il corpo dell'entità di risposta come matrice di byte senza segno. Questa matrice contiene i dati non elaborati ricevuti direttamente dal server.

## <a name="error-codes"></a>Codici di errore

Il valore restituito è **S \_ OK in caso** di esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce i dati della risposta in una matrice di byte senza segno. Se la risposta non ha un corpo della risposta, viene restituita una variante vuota. Questa proprietà può essere richiamata solo dopo la [**chiamata del**](iwinhttprequest-send.md) metodo Send.

> [!Note]  
> Per altre informazioni sull'implementazione Windows XP e Windows 2000, vedere [Requisiti di run-time](winhttp-start-page.md).

 

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

[**Responsestream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Versioni di WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




