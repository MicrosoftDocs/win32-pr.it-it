---
title: IAgentCommands sottotitoli
description: IAgentCommands sottotitoli
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398885"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands:: Caption

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Imposta il testo della [**didascalia**](caption-property.md) visualizzato per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR che specifica il valore per la proprietà [**Caption**](caption-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Impostando la proprietà [**Caption**](caption-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) , viene definita la modalità di visualizzazione nel menu popup del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su **true** e l'applicazione non è il client di input-Active. Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere.

Se si definiscono i comandi per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) per cui è impostata la [**didascalia**](caption-property.md) , in genere si definisce anche una **didascalia** per la raccolta di **comandi** .

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: sevisible**](iagentcommands--setvisible.md), [**IAgentCommands:: sevoice**](iagentcommands--setvoice.md)


 

 