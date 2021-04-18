---
title: External. Authenticate (metodo)
description: Il metodo Authenticate avvia un tentativo di autenticazione dell'utente.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- Metodo di autenticazione Media Player Windows
- metodo Authenticate Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo Authenticate
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
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328411"
---
# <a name="externalauthenticate-method"></a>External. Authenticate (metodo)

Il metodo **Authenticate** avvia un tentativo di autenticazione dell'utente.

## <a name="syntax"></a>Sintassi


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AuthenticationIndex* \[ in\]
</dt> <dd>

**Numero** (**Long**) che specifica l'indice di una pagina Web di autenticazione riuscita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Alcuni collegamenti in una pagina di individuazione hanno destinazioni che devono essere visualizzate solo dopo che l'utente è stato autenticato. La pagina di individuazione, Windows Media Player e il plug-in Online Store usano la procedura seguente per autenticare l'utente e visualizzare la pagina Web di destinazione:

1.  Script in una pagina di individuazione chiama l'oggetto *esterno*. metodo **Authenticate** .
2.  Windows Media Player visualizza una finestra di dialogo per ottenere un nome utente e una password.
3.  Windows Media Player chiama [IWMPContentPartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), che avvia il tentativo di autenticazione e restituisce immediatamente un risultato.
4.  Al termine del tentativo di autenticazione, il plug-in Online Store chiama [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnAuthResult e un valore booleano che indica se il tentativo ha avuto esito positivo.
5.  Se il tentativo di autenticazione ha avuto esito positivo, Windows Media Player chiama [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ AuthenticationSuccessURL, per ottenere l'URL di una pagina Web di autenticazione riuscita. In questa chiamata, Windows Media Player passa lo stesso indice che la pagina di individuazione passa a *External*. metodo **Authenticate** .
6.  Windows Media Player Visualizza la pagina Web autenticazione riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





