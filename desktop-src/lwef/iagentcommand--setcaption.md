---
title: IAgentCommand SetCaption
description: IAgentCommand SetCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ffccf42a972ec9635c929fb954d58bfaff967af364d24ae505e1dbb2bd8772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976361"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand::SetCaption

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Imposta il [**testo della**](caption-property.md) didascalia visualizzato per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Oggetto BSTR che specifica il testo per la proprietà [**Caption**](caption-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

L'impostazione della proprietà [**Caption**](caption-property.md) per un oggetto [**Command**](/windows/desktop/lwef/the-command-object) definisce come verrà visualizzato nel menu a comparsa del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su **True** e l'applicazione non è il client attivo per l'input. Per specificare un tasto di scelta (unlined mnemonic) per **caption,** includere un carattere e commerciale (&) prima di tale carattere. Per renderlo selezionabile, la [**relativa proprietà Enabled**](enabled-property.md) deve essere impostata su **True.**

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 