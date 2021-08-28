---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757b2d7554f1efcee27a519b9df61b4601a237b557c3aa26b6575864144a2850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105237"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Recupera il valore per il tipo di carattere visualizzato nel menu a comparsa del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Indirizzo di un BSTR che riceve il nome del tipo di carattere visualizzato nel menu a comparsa del carattere.

</dd> </dl>

Il nome del tipo di carattere restituito corrisponde al tipo di carattere usato per visualizzare il testo nel menu a comparsa del carattere quando l'applicazione client è attiva per l'input. Il valore predefinito per l'impostazione del tipo di carattere si basa sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere o, se non è impostato, sull'impostazione dell'ID lingua predefinita dell'utente.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




