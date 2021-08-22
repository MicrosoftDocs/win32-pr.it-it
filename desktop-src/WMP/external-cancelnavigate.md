---
title: Metodo External.cancelNavigate
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. | Metodo External.cancelNavigate
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- Metodo cancelNavigate Windows Media Player
- Metodo cancelNavigate Windows Media Player , classe external
- Classe esterna Windows Media Player metodo cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152594a427282a27c493f33f648b8a889a855f40a5fb13de69b7cc342099eed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649431"
---
# <a name="externalcancelnavigate-method"></a>Metodo External.cancelNavigate

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

Il **metodo cancelNavigate** Windows Media Player che non deve visualizzare una nuova pagina di individuazione anche se la visualizzazione è stata modificata in Player.

## <a name="syntax"></a>Sintassi


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando la visualizzazione cambia in Windows Media Player, Player chiama il plug-in del negozio online per determinare la pagina di individuazione da visualizzare successivamente. In alcuni casi, tuttavia, lo store online potrebbe richiedere al Lettore di continuare a visualizzare la pagina di individuazione esistente. Il processo seguente determina se player visualizza una nuova pagina di individuazione:

1.  Un'azione dell'utente, nell'interfaccia utente del lettore o nella pagina di individuazione, richiede al lettore di modificare la visualizzazione.
2.  Player chiama il metodo [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del plug-in per determinare la pagina di individuazione da visualizzare successivamente. Il lettore archivia l'URL della nuova pagina di individuazione, ma non visualizza la nuova pagina di individuazione in questo momento.
3.  Player genera [l'evento OnViewChange.](external-onviewchange-event.md)
4.  Se il **gestore dell'evento OnViewChange** nella pagina di individuazione chiama **cancelNavigate,** player non visualizza la nuova pagina di individuazione (determinata nel passaggio 2). Continua invece a visualizzare la pagina di individuazione esistente. Se il **gestore dell'evento OnViewChange** non chiama **cancelNavigate,** il lettore visualizza la nuova pagina di individuazione.

Si supponga, ad esempio, che il lettore attualmente visualizza la visualizzazione di un album con una determinata traccia selezionata. Si supponga anche che la pagina di individuazione corrente sia la pagina che rappresenta l'intero album. Se l'utente fa clic su una traccia diversa dallo stesso album, la visualizzazione del lettore cambia leggermente per mostrare che la nuova traccia è selezionata. Non è tuttavia necessario visualizzare una nuova pagina di individuazione. La pagina di individuazione che rappresenta l'intero album è comunque la pagina appropriata per la visualizzazione del lettore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





