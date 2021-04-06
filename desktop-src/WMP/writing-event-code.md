---
title: Scrittura del codice evento
description: Scrittura del codice evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player Skin, scrittura di codice
- interfacce, scrittura di codice
- eventi, scrittura di codice
- scrittura di codice per interfacce, informazioni
- Windows Media Player Skin, eventi
- interfacce, eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045321"
---
# <a name="writing-event-code"></a>Scrittura del codice evento

Gli eventi vengono trattati in modo analogo agli attributi. È necessario assegnare un valore all'evento e il valore è il codice che si desidera eseguire quando si verifica l'evento. La parola "on" viene aggiunta all'inizio del nome dell'evento; ad esempio, l'evento Click diventerà **OnClick**.

Il valore dell'evento è racchiuso tra virgolette doppie e inizia con la parola JScript seguita da due punti. Il codice che si vuole eseguire è successivo, seguito da un punto e virgola e dalle virgolette doppie di chiusura. Ad esempio, per arrestare la riproduzione quando l'utente fa clic su un pulsante, digitare quanto segue come attributo nel codice dell'elemento **Button** :


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Se si dispone di un codice che richiede virgolette, usare le virgolette singole. È necessario prestare attenzione quando si usano le virgolette in modo che siano bilanciate correttamente. Di seguito è riportato un esempio di utilizzo di entrambi i tipi:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



È anche possibile modificare gli attributi dell'interfaccia quando si gestisce un evento esterno. Per chiudere, ad esempio, una vista denominata visualizzazione, è possibile digitare:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi**](handling-events.md)
</dt> </dl>

 

 




