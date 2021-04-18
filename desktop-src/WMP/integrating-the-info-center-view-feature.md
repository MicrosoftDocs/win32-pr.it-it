---
title: Integrazione della funzionalità di visualizzazione del centro informazioni
description: Integrazione della funzionalità di visualizzazione del centro informazioni
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player Online Stores, integrazione della vista di Info Center
- negozi online, integrazione della vista di Info Center
- digitare 1 negozi online, integrazione della visualizzazione di Info Center
- digitare 2 archivi online, integrando la visualizzazione di Info Center
- Windows Media Player Online Stores, visualizzazione centro informazioni
- negozi online, visualizzazione centro informazioni
- digitare 1 negozi online, visualizzazione centro informazioni
- digitare 2 archivi online, visualizzazione centro informazioni
- integrazione di visualizzazione centro informazioni
- Visualizzazione centro informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298847"
---
# <a name="integrating-the-info-center-view-feature"></a>Integrazione della funzionalità di visualizzazione del centro informazioni

Windows Media Player consente agli utenti di aprire e chiudere la funzionalità Visualizzazione del centro informazioni. La visualizzazione centro informazioni è la funzionalità in cui gli utenti si aspettano di trovare informazioni dettagliate e estese su contenuto multimediale digitale specifico. Quando l'utente sceglie di aprire la visualizzazione del centro informazioni, Windows Media Player chiama sull'archivio musica corrente per visualizzare la pagina Web visualizzazione del centro informazioni specificata dall'attributo **URL** **dell'elemento del** centro informazioni del documento ServiceInfo.

Per recuperare informazioni sul contenuto multimediale digitale attualmente in riproduzione, è necessario incorporare un'istanza del controllo Media Player Windows nella pagina Web e utilizzare il modello a oggetti del lettore. Per recuperare il titolo, ad esempio, è possibile usare il codice JScript seguente:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Linee guida per la visualizzazione centro informazioni

Quando si crea la pagina Web **visualizzazione centro informazioni** , attenersi alle linee guida seguenti:

-   La pagina deve identificare chiaramente l'archivio online che fornisce le informazioni. A tale scopo, è possibile visualizzare in primo piano il logo, ad esempio.
-   La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.
-   Evitare l'esplorazione delle pagine all'interno della funzionalità di visualizzazione del centro informazioni quando possibile. Per la maggior parte delle attività, è necessario passare all'archivio online.
-   È preferibile fornire informazioni preziose senza richiedere all'utente di installare programmi o accedere al proprio negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Elemento centro informazioni**](infocenter-element.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in una pagina Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




