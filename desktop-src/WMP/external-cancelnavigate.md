---
title: External. cancelNavigate, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. cancelNavigate, metodo
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- Metodo cancelNavigate Windows Media Player
- Metodo cancelNavigate Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo cancelNavigate
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
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331237"
---
# <a name="externalcancelnavigate-method"></a>External. cancelNavigate, metodo

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **cancelNavigate** informa Windows Media Player che non dovrebbe visualizzare una nuova pagina di individuazione anche se la visualizzazione è cambiata nel lettore.

## <a name="syntax"></a>Sintassi


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando la visualizzazione cambia in Windows Media Player, il lettore chiama il plug-in Online Store per determinare la pagina di individuazione da visualizzare successivamente. In alcuni casi, tuttavia, l'archivio online potrebbe volere che il lettore continui a visualizzare la pagina di individuazione esistente. Il processo seguente determina se il lettore Visualizza una nuova pagina di individuazione:

1.  Un'azione da parte dell'utente, nell'interfaccia utente del lettore o nella pagina di individuazione, richiede che il lettore modifichi la propria visualizzazione.
2.  Il lettore chiama il metodo [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del plug-in per determinare la pagina di individuazione da visualizzare successivamente. Il lettore archivia l'URL della nuova pagina di individuazione, ma non Visualizza la nuova pagina di individuazione in questo momento.
3.  Il lettore genera l'evento [OnViewChange](external-onviewchange-event.md) .
4.  Se il gestore dell'evento **OnViewChange** nella pagina di individuazione chiama **CancelNavigate**, il lettore non Visualizza la nuova pagina di individuazione (determinata nel passaggio 2). Ma continua a visualizzare la pagina di individuazione esistente. Se il gestore dell'evento **OnViewChange** non chiama **CancelNavigate**, il lettore Visualizza la nuova pagina di individuazione.

Si supponga, ad esempio, che il lettore stia visualizzando la visualizzazione di un album con una certa traccia selezionata. Si supponga inoltre che la pagina di individuazione corrente sia la pagina che rappresenta l'intero album. Se l'utente fa clic su una traccia diversa dallo stesso album, la visualizzazione del giocatore cambia leggermente per indicare che la nuova traccia è selezionata. Non è tuttavia necessario visualizzare una nuova pagina di individuazione. La pagina di individuazione che rappresenta l'intero album è ancora la pagina appropriata per la visualizzazione del lettore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





