---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e27996f06a0446f7aaab944df8638134990fffe951400d94c690f52f78cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750428"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand::GetVoice

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Recupera il valore della proprietà [**Testo**](voice-property.md) vocale per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Indirizzo di un oggetto BSTR che riceve la [**proprietà Voice**](voice-property.md) text per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) con la [**proprietà Voice**](voice-property.md) impostata e la relativa proprietà [**Enabled**](enabled-property.md) impostata su **True** sarà accessibile tramite voce. Se è impostata anche la proprietà [**Caption,**](caption-property.md) viene visualizzata nella finestra Comandi vocali. Se la [**proprietà Visible**](visible-property.md) è **impostata su True,** viene visualizzata nel menu a comparsa del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 