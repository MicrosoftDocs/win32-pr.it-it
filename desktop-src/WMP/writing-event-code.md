---
title: Scrittura di codice evento
description: Scrittura di codice evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player, scrittura di codice
- interfaccia, scrittura di codice
- eventi, scrittura di codice
- scrittura di codice per le interfaccia, informazioni
- Windows Media Player, eventi
- interfaccia, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39c35864151db1671c2f7fa94caea803f0a33cc1082a3ae44082a90f7bddafb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760571"
---
# <a name="writing-event-code"></a>Scrittura di codice evento

Gli eventi vengono trattati in modo analogo agli attributi. È necessario assegnare un valore all'evento e il valore è il codice che si vuole eseguire quando si verifica l'evento. La parola "on" viene aggiunta all'inizio del nome dell'evento. Ad esempio, l'evento click diventerà **onclick**.

Il valore dell'evento è racchiuso tra virgolette doppie e inizia con la parola JScript seguito da due punti. Il codice da eseguire è successivo, seguito da un punto e virgola e dalle virgolette doppie di chiusura. Ad esempio, per interrompere la riproduzione quando l'utente fa clic su un pulsante, digitare quanto segue come attributo nel codice **dell'elemento BUTTON:**


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Se si dispone di un codice che richiede virgolette, usare le virgolette singole. È necessario fare attenzione quando si usano le virgolette in modo che siano bilanciate correttamente. Di seguito è riportato un esempio dell'uso di entrambi i tipi:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



È anche possibile modificare gli attributi dell'interfaccia durante la gestione di un evento esterno. Ad esempio, per chiudere una visualizzazione denominata myView, è possibile digitare:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi**](handling-events.md)
</dt> </dl>

 

 




