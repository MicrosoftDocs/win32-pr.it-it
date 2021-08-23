---
title: Metodo External.attemptLogin
description: Il metodo attemptLogin visualizza una finestra di dialogo in modo che l'utente possa tentare di accedere al negozio online.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Metodo attemptLogin Windows Media Player
- metodo attemptLogin Windows Media Player , classe external
- Classe esterna Windows Media Player metodo , attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f967e812ff76dd11dfd9b4ff07a542d2575548519c3a52816fadf6302a719d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649541"
---
# <a name="externalattemptlogin-method"></a>Metodo External.attemptLogin

Il **metodo attemptLogin** visualizza una finestra di dialogo in modo che l'utente possa tentare di accedere al negozio online.

## <a name="syntax"></a>Sintassi


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il tentativo di accesso comporta una modifica dello stato di accesso, Windows Media Player genera [l'evento OnLoginChange.](external-onloginchange-event.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Evento External.OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner::Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Gestione dell'account di accesso**](managing-login.md)
</dt> </dl>

 

 





