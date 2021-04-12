---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396194"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx:: GetFontSize

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Recupera il valore per la dimensione del tipo di carattere visualizzato nel menu di scelta rapida del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Indirizzo di un valore che riceve la dimensione del tipo di carattere.

</dd> </dl>

La dimensione in punti del tipo di carattere restituito corrisponde alla dimensione definita per visualizzare il testo nel menu popup del carattere quando il client è di input-attivo. Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere oppure, se non è impostato, l'impostazione della lingua predefinita dell'utente.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx:: sefontsize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx:: sefontname**](iagentcommandsex--setfontname.md)


 

 




