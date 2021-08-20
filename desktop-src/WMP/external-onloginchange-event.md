---
title: Evento External.OnLoginChange
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. | Evento External.OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Evento External.OnLoginChange Windows Media Player
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
ms.openlocfilehash: a0697aff759309bc3a988e6f24a024d5c05bd8ec27dae85921ee09d3847f3dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648741"
---
# <a name="externalonloginchange-event"></a>Evento External.OnLoginChange

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'evento OnLoginChange** si verifica quando lo stato di accesso dell'utente cambia o quando un tentativo di accesso ha esito negativo.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiamate quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento non accetta parametri.

## <a name="remarks"></a>Commenti

Questo evento si verifica ogni volta che il plug-in dello store online chiama [IWMPContentPartnerCallback::Notify,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)passando wmpcnLoginStateChange nel parametro *di* tipo. In alcuni casi il plug-in effettua questa chiamata per notificare Windows Media Player che è stata apportata una modifica allo stato di accesso dell'utente. Altre volte, il plug-in effettua questa chiamata per notificare al lettore che un tentativo di accesso non è riuscito. Il *parametro pContext* del **metodo Notify** specifica se la notifica è relativa a una modifica dello stato di accesso o a un tentativo di accesso non riuscito.

Poiché ogni chiamata a determina la generazione dell'evento OnLoginChange da parte di Windows Media Player, il gestore eventi `Notify(wmpcnLoginStateChange, ...)` **OnLoginChange** viene chiamato a volte come risultato di una modifica dello stato di accesso e talvolta come risultato di un tentativo di accesso non riuscito.  Per determinare lo stato di accesso corrente dell'utente, il gestore eventi **OnLoginChange** deve chiamare [External.userLoggedIn](external-userloggedin.md).

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

 

 





