---
description: Consente alle pagine sul lato server ospitate in una procedura guidata di verificare che l'utente sia stato autenticato tramite un account Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Metodo NewWDEvents.PassportAuthenticate (Shldisp.h)
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
ms.openlocfilehash: f462053281efd97b75422c55ce23829688d18ac153ecb92c7544eafb8f356b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942401"
---
# <a name="newwdeventspassportauthenticate-method"></a>Metodo NewWDEvents.PassportAuthenticate

Consente alle pagine sul lato server ospitate in una procedura guidata di verificare che l'utente sia stato autenticato tramite un account Microsoft.

## <a name="syntax"></a>Sintassi


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrSignInUrl* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Stringa contenente l'URL di una pagina Web che reindirizza all'interfaccia account Microsoft'interfaccia utente di accesso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Boolean**

Impostare su **true se l'autenticazione** ha esito positivo, **false in caso** contrario.

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato anche se un utente è già connesso a un account Microsoft. In tal caso, il metodo restituisce **true** senza visualizzare il account Microsoft di accesso all'interfaccia utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 6.0 o successiva)</dt> </dl> |



 

 
