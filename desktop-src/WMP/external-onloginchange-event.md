---
title: Evento External. OnLoginChange
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Media Player di Windows dell'evento External. OnLoginChange
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324559"
---
# <a name="externalonloginchange-event"></a>Evento External. OnLoginChange

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'evento **OnLoginChange** si verifica quando lo stato di accesso dell'utente cambia o quando un tentativo di accesso ha esito negativo.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento non accetta parametri.

## <a name="remarks"></a>Commenti

Questo evento si verifica ogni volta che il plug-in Online Store chiama [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange nel parametro di *tipo* . A volte il plug-in effettua questa chiamata per notificare a Windows Media Player che si è verificata una modifica nello stato di accesso dell'utente. In altri casi, il plug-in effettua questa chiamata per notificare al lettore che un tentativo di accesso non è riuscito. Il parametro *pContext* del metodo **Notify** specifica se la notifica è relativa a una modifica dello stato di accesso o a un tentativo di accesso non riuscito.

Poiché ogni chiamata a `Notify(wmpcnLoginStateChange, ...)` fa in modo che Windows Media Player generi l'evento **OnLoginChange** , il gestore eventi **OnLoginChange** viene chiamato a volte come il risultato di una modifica nello stato di accesso e talvolta come il risultato di un tentativo di accesso non riuscito. Per determinare lo stato di accesso corrente dell'utente, è necessario che il gestore dell'evento **OnLoginChange** chiami [External. userLoggedIn](external-userloggedin.md).

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

 

 





