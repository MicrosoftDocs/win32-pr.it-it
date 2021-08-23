---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b38138d218804461afc782efc14ff3685f55d2f737db6fdb21c39021efbcb36e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665471"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands::SetCaption

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Imposta il [**testo della**](caption-property.md) didascalia visualizzato per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Oggetto BSTR che specifica il valore della proprietà [**Caption**](caption-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

L'impostazione della proprietà [**Caption**](caption-property.md) per una raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) definisce come verrà visualizzato nel menu a comparsa del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su **True** e l'applicazione non è il client attivo per l'input. Per specificare un tasto di scelta (unlined mnemonic) per **caption,** includere un carattere e commerciale (&) prima di tale carattere.

Se si definiscono comandi per una [**raccolta Commands**](/windows/desktop/lwef/the-commands-collection-object) con la proprietà [**Caption**](caption-property.md) impostata, in genere si definisce anche **una didascalia** per la **relativa raccolta Commands.**

## <a name="see-also"></a>Vedere anche

[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)


 

 