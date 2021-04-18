---
description: Imposta i criteri di accesso automatici correnti.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'Metodo IWinHttpRequest:: SetAutoLogonPolicy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316004"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>Metodo IWinHttpRequest:: SetAutoLogonPolicy

Il metodo **SetAutoLogonPolicy** imposta i [criteri di accesso automatici](authentication-in-winhttp.md)correnti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AutoLogonPolicy* \[ in\]
</dt> <dd>

Specifica i criteri di accesso automatici correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Il criterio predefinito è [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).

Chiamare **SetAutoLogonPolicy** per impostare i criteri di accesso automatici prima di chiamare [**Send**](iwinhttprequest-send.md) per inviare la richiesta.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="examples"></a>Esempio

Nell'esempio di script seguente viene illustrato come impostare i criteri di accesso automatici in modo da non utilizzare mai NTLM o negoziare automaticamente l'autenticazione.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



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

[Autenticazione in WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




