---
title: IAgentCommands GetVoice
description: IAgentCommands GetVoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b348904020a53eb11d2bb7884a05f8d98e223a359f796e7d891dafb3dcc402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105336"
---
# <a name="iagentcommandsgetvoice"></a>IAgentCommands::GetVoice

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

Recupera il valore della proprietà [**Voice**](voice-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Indirizzo di un oggetto BSTR che riceve il valore dell'impostazione [**Di**](voice-property.md) testo vocale per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommands::SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md)


 

 