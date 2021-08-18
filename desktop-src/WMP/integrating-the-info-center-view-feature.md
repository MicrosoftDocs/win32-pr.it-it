---
title: Integrazione della funzionalità di visualizzazione del Centro informazioni
description: Integrazione della funzionalità di visualizzazione del Centro informazioni
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player negozi online, integrazione della visualizzazione info center
- negozi online, integrazione della visualizzazione info center
- Tipo 1 di negozi online, integrazione della visualizzazione del Centro informazioni
- Tipo 2 di negozi online, integrazione della visualizzazione info center
- Windows Media Player negozi online, Visualizzazione Info Center
- negozi online,Visualizzazione Info Center
- Tipo 1 di negozi online, Visualizzazione Info Center
- Tipo 2 di negozi online, Visualizzazione Info Center
- integrazione della visualizzazione del Centro informazioni
- Visualizzazione del Centro informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caea279f933c3cbb411da72aab9ddf971df5f38c69d7291ae4ac67f7b96ed91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135464"
---
# <a name="integrating-the-info-center-view-feature"></a>Integrazione della funzionalità di visualizzazione del Centro informazioni

Windows Media Player consente agli utenti di aprire e chiudere la funzionalità Visualizzazione Info Center. La visualizzazione info center è la funzionalità in cui gli utenti si aspettano di trovare informazioni dettagliate ed estese su contenuti multimediali digitali specifici. Quando l'utente sceglie di aprire la visualizzazione info center, Windows Media Player chiama il negozio di musica corrente per visualizzare la pagina Web di Visualizzazione Info Center specificata dall'attributo **URL** dell'elemento **InfoCenter** del documento ServiceInfo.

Per recuperare informazioni sul contenuto multimediale digitale attualmente in riproduzione, è necessario incorporare un'istanza del controllo Windows Media Player nella pagina Web e usare il modello a oggetti player. Ad esempio, per recuperare il titolo, è possibile usare il codice JScript seguente:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Linee guida per la visualizzazione del Centro informazioni

Quando si crea la **pagina Web di Visualizzazione Info Center,** usare le linee guida seguenti:

-   La pagina deve identificare chiaramente il negozio online che fornisce le informazioni. A tale scopo, ad esempio, è possibile visualizzare in primo piano il logo.
-   La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.
-   Evitare lo spostamento tra le pagine all'interno della funzionalità Visualizzazione Info Center, quando possibile. È consigliabile passare al negozio online per la maggior parte delle attività.
-   È meglio fornire informazioni preziose senza richiedere all'utente di installare programmi o accedere al negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Elemento InfoCenter**](infocenter-element.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Uso del Windows Media Player controllo in una pagina Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




