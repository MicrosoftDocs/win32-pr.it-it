---
description: Abilita le pagine lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Metodo NewWDEvents. PassportAuthenticate (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760514"
---
# <a name="newwdeventspassportauthenticate-method"></a>NewWDEvents. PassportAuthenticate, metodo

Abilita le pagine lato server ospitate in una procedura guidata per verificare che l'utente sia stato autenticato tramite un account Microsoft.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrSignInUrl* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Stringa contenente l'URL di una pagina Web che reindirizza all'interfaccia utente di accesso account Microsoft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **booleano**

Impostare su **true** se l'autenticazione ha esito positivo; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato anche se un utente è già connesso a un account Microsoft. In tal caso, il metodo restituisce **true** senza visualizzare l'account Microsoft l'interfaccia utente di accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 6,0 o successiva)</dt> </dl> |



 

 
