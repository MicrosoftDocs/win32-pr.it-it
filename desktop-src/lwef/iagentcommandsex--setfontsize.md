---
title: IAgentCommandsEx sefontsize
description: IAgentCommandsEx sefontsize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472859"
---
# <a name="iagentcommandsexsetfontsize"></a>IAgentCommandsEx:: sefontsize

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

Imposta la dimensione del tipo di carattere visualizzato nel menu di scelta rapida del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Dimensione del carattere.

</dd> </dl>

Questa proprietà determina la dimensione in punti del tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere quando l'applicazione client è di input-attivo. Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere, o se non è impostato, l'impostazione della lingua predefinita dell'utente. Se l'opzione non è attiva, il testo della [](/windows/desktop/lwef/the-command-object) [**didascalia**](caption-property.md) del comando dell'applicazione client viene visualizzato nelle dimensioni dei punti specificate per il client attivo di input.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx:: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: sefontname**](iagentcommandsex--setfontname.md)


 

 