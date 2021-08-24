---
title: Metodo External.authenticate
description: Il metodo authenticate avvia un tentativo di autenticazione dell'utente.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- Metodo authenticate Windows Media Player
- Metodo authenticate Windows Media Player , classe external
- Metodo di autenticazione Windows Media Player classe esterna
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b72c4d20cdd8232746175d966856a616bca9629657ca66c35727b8af8e21178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649551"
---
# <a name="externalauthenticate-method"></a>Metodo External.authenticate

Il **metodo authenticate** avvia un tentativo di autenticazione dell'utente.

## <a name="syntax"></a>Sintassi


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AuthenticationIndex* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) che specifica l'indice di una pagina Web di autenticazione riuscita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Alcuni collegamenti in una pagina di individuazione hanno destinazioni che devono essere visualizzate solo dopo l'autenticazione dell'utente. La pagina di individuazione, Windows Media Player e il plug-in del negozio online usano la procedura seguente per autenticare l'utente e visualizzare la pagina Web di destinazione:

1.  Lo script in una pagina di individuazione chiama *external*. **metodo authenticate.**
2.  Windows Media Player una finestra di dialogo per ottenere un nome utente e una password.
3.  Windows Media Player chiama [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), che avvia il tentativo di autenticazione e restituisce immediatamente .
4.  Al termine del tentativo di autenticazione, il plug-in dello store online chiama [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnAuthResult e un valore booleano che indica se il tentativo è riuscito.
5.  Se il tentativo di autenticazione ha avuto esito positivo, Windows Media Player chiama [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo AuthenticationSuccessURL, per ottenere l'URL di una pagina Web di autenticazione \_ riuscita. In questa chiamata, Windows Media Player lo stesso indice passato dalla pagina di individuazione a *External*. **metodo authenticate.**
6.  Windows Media Player visualizza la pagina Web authentication-success.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





