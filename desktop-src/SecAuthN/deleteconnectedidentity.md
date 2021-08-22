---
description: Elimina le credenziali utente usate per l'identità connessa.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Funzione DeleteConnectedIdentity (Indentitystore.h)
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
ms.openlocfilehash: 7e59beeb17f7d6d0cced96daaceef7440523c3ce603d759f18cc69a93c0ab05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008469"
---
# <a name="deleteconnectedidentity-function"></a>Funzione DeleteConnectedIdentity

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

*ProviderHandle* \[ Pollici\]
</dt> <dd>

Handle del provider di identità.

</dd> <dt>

*UserToken* \[ in, facoltativo\]
</dt> <dd>

Token dell'utente connesso il cui account verrà convertito in un account locale. Se *UserToken* non è **NULL,** il provider di identità usa questo token per caricare il profilo utente e pulire gli stati connessi. Se *UserToken* è **NULL,** LSA forza la disconnessione. Il provider di identità deve pulire tutti gli stati connessi globali per questo utente, ma il provider non deve pulire gli stati connessi nel profilo utente.

</dd> <dt>

*UserSid* \[ Pollici\]
</dt> <dd>

SID primario dell'utente connesso. Se *UserToken* non è **NULL,** questo parametro è il SID utente del token. Se *UserToken* è **NULL,** questo parametro viene usato per identificare l'utente connesso e pulire gli stati di connessione globali dell'utente.

</dd> <dt>

*IdentityUserName* \[ Pollici\]
</dt> <dd>

Nome utente dell'identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.

Se la funzione ha esito negativo, la funzione può restituire uno dei codici di errore seguenti.



| Valore restituito                                                                                               | Descrizione                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>PARAMETRO \_ STATUS NON \_ VALIDO</dt> </dl>      | Un parametro non è valido.<br/>                                                                                                                        |
| <dl> <dt>STATO \_ NESSUN UTENTE DI QUESTO \_ \_ TIPO</dt> </dl>          | L'utente identificato da *UserSid* non esiste, non è attualmente connesso o non esiste alcuna identità il cui nome utente corrisponde *a IdentityUserName.*<br/> |
| <dl> <dt>RISORSE \_ INSUFFICIENTI DI \_ STATO</dt> </dl> | Memoria insufficiente per elaborare la richiesta.<br/>                                                                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Indentitystore.h</dt> </dl> |



 

 




