---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb0bceae040f9261d2530b19d074df937dbdaf80d91a27f57b5cf9c1fd8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725319"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon::GetFontName

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Recupera il valore per il tipo di carattere visualizzato in un fumetto di parole.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Indirizzo di un BSTR che riceve il nome del tipo di carattere visualizzato in un fumetto.

</dd> </dl>

Il tipo di carattere predefinito usato in un fumetto di parole di tipo carattere è definito nell'editor di caratteri di Microsoft Agent. È possibile modificarlo con [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**). L'utente può eseguire l'override dell'impostazione del carattere per tutti i caratteri usando la finestra delle proprietà di Microsoft Agent.

 

 




