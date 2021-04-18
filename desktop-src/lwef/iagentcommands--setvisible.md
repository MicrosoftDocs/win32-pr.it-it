---
title: IAgentCommands visibile
description: IAgentCommands visibile
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299608"
---
# <a name="iagentcommandssetvisible"></a>IAgentCommands:: sevisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Imposta il valore della proprietà [**Visible**](visible-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Valore booleano che determina la proprietà [**Visible**](visible-property.md) di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . **True** imposta la [**didascalia**](caption-property.md) della raccolta di **comandi** in modo che sia visibile quando viene visualizzato il menu popup del carattere; *False* non lo Visualizza.

</dd> </dl>

Una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) deve avere la relativa proprietà [**Caption**](caption-property.md) impostata e la relativa proprietà [**Visible**](visible-property.md) impostata su **true** per essere visualizzata nel menu popup del carattere. È inoltre necessario impostare la proprietà **Visible** su **true** per visualizzare i comandi della raccolta quando l'applicazione client è di input-Active.

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: getVisible**](iagentcommands--getvisible.md), [ **IAgentCommand:: Caption**](iagentcommand--setcaption.md)


 

 