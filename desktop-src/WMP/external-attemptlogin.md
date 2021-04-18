---
title: External. attemptLogin, metodo
description: Il metodo attemptLogin Visualizza una finestra di dialogo in modo che l'utente possa tentare di accedere al negozio online.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Metodo attemptLogin Windows Media Player
- Metodo attemptLogin Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo attemptLogin
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
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328412"
---
# <a name="externalattemptlogin-method"></a>External. attemptLogin, metodo

Il metodo **attemptLogin** Visualizza una finestra di dialogo in modo che l'utente possa tentare di accedere al negozio online.

## <a name="syntax"></a>Sintassi


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il tentativo di accesso comporta una modifica dello stato di accesso, Windows Media Player genera l'evento [OnLoginChange](external-onloginchange-event.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Evento External. OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner:: login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Gestione dell'accesso**](managing-login.md)
</dt> </dl>

 

 





