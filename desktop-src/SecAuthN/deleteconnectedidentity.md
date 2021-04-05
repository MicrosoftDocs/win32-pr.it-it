---
description: Elimina le credenziali utente usate per l'identità connessa.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Funzione DeleteConnectedIdentity (Indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049366"
---
# <a name="deleteconnectedidentity-function"></a>DeleteConnectedIdentity (funzione)

Elimina le credenziali utente usate per l'identità connessa.

## <a name="syntax"></a>Sintassi


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProviderHandle* \[ in\]
</dt> <dd>

Handle del provider di identità.

</dd> <dt>

*UserToken* \[ in, facoltativo\]
</dt> <dd>

Token dell'utente connesso il cui account verrà convertito in un account locale. Se *userToken* non è **null**, il provider di identità utilizza questo token per caricare il profilo utente e pulire gli stati connessi. Se *userToken* è **null**, LSA forza la disconnessione. Il provider di identità deve pulire tutti gli stati connessi globali per questo utente, ma non è necessario che il provider ripulisca gli stati connessi nel profilo utente.

</dd> <dt>

*UserSID* \[ in\]
</dt> <dd>

SID primario dell'utente connesso. Se *userToken* non è **null**, questo parametro è il SID utente del token. Se *userToken* è **null**, questo parametro viene usato per identificare l'utente connesso e pulire gli Stati di connessione globale di tale utente.

</dd> <dt>

*IdentityUserName* \[ in\]
</dt> <dd>

Nome utente dell'identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, la funzione può restituire uno dei codici di errore seguenti.



| Valore restituito                                                                                               | Descrizione                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>STATO \_ parametro non valido \_</dt> </dl>      | Un parametro non è valido.<br/>                                                                                                                        |
| <dl> <dt>STATO \_ senza \_ tale \_ utente</dt> </dl>          | L'utente identificato da *UserSID* non esiste, non è attualmente connesso o non esiste alcuna identità il cui nome utente corrisponde a *IdentityUserName*.<br/> |
| <dl> <dt>STATO \_ risorse insufficienti \_</dt> </dl> | Memoria insufficiente per elaborare la richiesta.<br/>                                                                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Indentitystore. h</dt> </dl> |



 

 




