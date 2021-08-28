---
title: Evento External.OnViewChange
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato. L'evento OnViewChange si verifica quando la visualizzazione cambia in Windows Media Player.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Evento External.OnViewChange Windows Media Player
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c01db02ef1bfd194330483c8dd7e71eba7ed09d9b347aee4b4813f413950c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648681"
---
# <a name="externalonviewchange-event"></a>Evento External.OnViewChange

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

**L'evento OnViewChange** si verifica quando la visualizzazione cambia in Windows Media Player.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento non accetta parametri.

## <a name="remarks"></a>Commenti

La visualizzazione in Windows Media Player può cambiare per uno dei motivi seguenti:

-   L'utente interagisce con l'Windows Media Player utente.
-   L'utente interagisce con una pagina di individuazione e lo script nella pagina di individuazione chiama [External.changeView.](external-changeview.md)
-   L'utente interagisce con una pagina di individuazione e lo script nella pagina di individuazione chiama [External.changeViewOnlineList.](external-changeviewonlinelist.md)

Quando la visualizzazione cambia in Windows Media Player, il lettore chiama [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) per ottenere l'URL della pagina di individuazione successiva da visualizzare. Tuttavia, prima che il lettore visualizzi la nuova pagina di individuazione, genera **l'evento OnViewChange.** Se il **gestore dell'evento OnViewChange** chiama [External.cancelNavigate,](external-cancelnavigate.md)Windows Media Player non visualizza la nuova pagina di individuazione. Continua invece a visualizzare la pagina di individuazione corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeView**](external-changeview.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





