---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979651635c27f5633d5ebeada8e5f2866d383ece0b19a38dd32082596e4712b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692781"
---
# <a name="iagentcommandssetvisible"></a>IAgentCommands::SetVisible

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Imposta il valore della [**proprietà Visible**](visible-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valore booleano che determina la [**proprietà Visible**](visible-property.md) di una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) **True** imposta **la didascalia** della raccolta [**Commands**](caption-property.md) in modo che sia visibile quando viene visualizzato il menu a comparsa del carattere. *False* non lo visualizza.

</dd> </dl>

Una [**raccolta Commands**](/windows/desktop/lwef/the-commands-collection-object) deve avere la proprietà [**Caption**](caption-property.md) impostata e la relativa proprietà [**Visible**](visible-property.md) impostata su **True** per essere visualizzata nel menu a comparsa del carattere. La **proprietà Visible** deve anche essere impostata su **True** perché i comandi nella raccolta vengano visualizzati quando l'applicazione client è attiva per l'input.

## <a name="see-also"></a>Vedere anche

[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [ **IAgentCommand::SetCaption**](iagentcommand--setcaption.md)


 

 