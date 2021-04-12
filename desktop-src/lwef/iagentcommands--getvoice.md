---
title: IAgentCommands getvoice
description: IAgentCommands getvoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399025"
---
# <a name="iagentcommandsgetvoice"></a>IAgentCommands:: getvoice

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

Recupera il valore della proprietà [**Voice**](voice-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore dell'impostazione del testo [**vocale**](voice-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: sevoice**](iagentcommands--setvoice.md), [**IAgentCommands:: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: getVisible**](iagentcommands--getvisible.md)


 

 