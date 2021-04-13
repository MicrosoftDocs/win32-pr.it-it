---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396803"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon:: GetFontName

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Recupera il valore per il tipo di carattere visualizzato in un fumetto di Word.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Indirizzo di un BSTR che riceve il nome del tipo di carattere visualizzato in un fumetto di Word.

</dd> </dl>

Il tipo di carattere predefinito utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent. È possibile modificarlo con [**IAgentBalloon:: Sefontname**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**). L'utente può eseguire l'override dell'impostazione del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.

 

 




