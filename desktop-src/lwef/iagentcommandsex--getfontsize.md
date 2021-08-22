---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f2ce1908ea5f37d24fb8a085204917440f61ae30feb1e596639d0240c353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976271"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx::GetFontSize

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Recupera il valore per le dimensioni del tipo di carattere visualizzato nel menu a comparsa del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Indirizzo di un valore che riceve le dimensioni del tipo di carattere.

</dd> </dl>

Le dimensioni in punti del tipo di carattere restituito corrispondono alle dimensioni definite per visualizzare il testo nel menu a comparsa del carattere quando il client è attivo per l'input. Il valore predefinito per l'impostazione del tipo di carattere si basa sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere oppure, se non è impostata, sull'impostazione della lingua predefinita dell'utente.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)


 

 




