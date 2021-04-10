---
title: IAgentCommand sottotitoli
description: IAgentCommand sottotitoli
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88453f54ffa59b413f30d27c58aa6cd2dcc6e12e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046665"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand:: Caption

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Imposta il testo della [**didascalia**](caption-property.md) visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR che specifica il testo per la proprietà [**Caption**](caption-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

L'impostazione della proprietà [**Caption**](caption-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) ne definisce la modalità di visualizzazione nel menu popup del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su **true** e l'applicazione non è il client di input-Active. Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere. Per renderla selezionabile, la relativa proprietà [**Enabled**](enabled-property.md) deve essere impostata su **true**.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: seenabled**](iagentcommand--setenabled.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 