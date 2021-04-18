---
description: Recupera il corpo dell'entità della risposta come matrice di byte senza segno.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'Proprietà IWinHttpRequest:: ResponseBody'
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
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318196"
---
# <a name="iwinhttprequestresponsebody-property"></a>Proprietà IWinHttpRequest:: ResponseBody

La proprietà **responseBody** Recupera il corpo dell'entità della risposta come matrice di byte senza segno.

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

Valore **Variant** che riceve il corpo dell'entità della risposta come matrice di byte senza segno. Questa matrice contiene i dati non elaborati ricevuti direttamente dal server.

## <a name="error-codes"></a>Codici di errore

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Questa proprietà restituisce i dati di risposta in una matrice di byte senza segno. Se la risposta non ha un corpo della risposta, viene restituita una variante vuota. Questa proprietà può essere richiamata solo dopo la chiamata del metodo [**Send**](iwinhttprequest-send.md) .

> [!Note]  
> Per ulteriori informazioni sull'implementazione per Windows XP e Windows 2000, vedere [requisiti di run-time](winhttp-start-page.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




