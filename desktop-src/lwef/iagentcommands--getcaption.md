---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6eb40b0be58695e79a02ab0ad67ad0d26a47bd13a1637dc1d1f5a4380a7429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749887"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands::GetCaption

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Recupera la [**didascalia per**](caption-property.md) una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore dell'impostazione [**Testo**](caption-property.md) didascalia visualizzato per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)


 

 