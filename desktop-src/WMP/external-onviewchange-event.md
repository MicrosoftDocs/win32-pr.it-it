---
title: Evento External. OnViewChange
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'evento OnViewChange si verifica quando la visualizzazione cambia in Windows Media Player.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Media Player di Windows dell'evento External. OnViewChange
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
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324555"
---
# <a name="externalonviewchange-event"></a>Evento External. OnViewChange

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'evento **OnViewChange** si verifica quando la visualizzazione cambia in Windows Media Player.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento non accetta parametri.

## <a name="remarks"></a>Commenti

La visualizzazione in Windows Media Player può variare per uno dei seguenti motivi:

-   L'utente interagisce con l'interfaccia utente di Windows Media Player.
-   L'utente interagisce con una pagina di individuazione e lo script nella pagina di individuazione chiama [External. changeView](external-changeview.md).
-   L'utente interagisce con una pagina di individuazione e lo script nella pagina di individuazione chiama [External. changeViewOnlineList](external-changeviewonlinelist.md).

Quando la visualizzazione cambia in Windows Media Player, il lettore chiama [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) per ottenere l'URL della pagina di individuazione successiva da visualizzare. Tuttavia, prima che il lettore visualizzi la nuova pagina di individuazione, genera l'evento **OnViewChange** . Se il gestore dell'evento **OnViewChange** chiama [External. cancelNavigate](external-cancelnavigate.md), Windows Media Player non Visualizza la nuova pagina di individuazione. Ma continua a visualizzare la pagina di individuazione corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





