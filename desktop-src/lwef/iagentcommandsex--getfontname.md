---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396195"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx:: GetFontName

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Recupera il valore per il tipo di carattere visualizzato nel menu di scelta rapida del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Indirizzo di un BSTR che riceve il nome del tipo di carattere visualizzato nel menu di scelta rapida del carattere.

</dd> </dl>

Il nome del tipo di carattere restituito corrisponde al tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere quando l'applicazione client è di input-attivo. Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere oppure, se non è impostato, l'impostazione dell'ID lingua predefinita dell'utente.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx:: sefontname**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx:: sefontsize**](iagentcommandsex--setfontsize.md)


 

 




