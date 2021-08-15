---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533f9cb05143d4948fbcae1f8d9ed74a7216c5a2520b28f4c299321bcbac4272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478030"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx::GetActive

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Recupera un valore che indica se l'applicazione client è il client attivo del carattere e se il carattere è in primo piano.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Indirizzo di una variabile che riceve uno dei valori seguenti per l'impostazione dello stato:



| Valore                                                              | Descrizione                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | Il client non è il client attivo del carattere.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | Il client è il client attivo del carattere.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | Il client è attivo di input (client attivo del carattere in primo piano). |



 

</dd> </dl>

Questa impostazione consente di sapere se si è il client attivo del carattere o se il carattere è il carattere attivo di input. Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse, ad esempio eventi di clic o trascinamento del controllo di Microsoft Agent. Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere in primo piano (noto anche come client attivo di input) riceve gli eventi [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

Usare il [**metodo Activate**](iagentcharacter--activate.md) per impostare se l'applicazione è il client attivo del carattere o per impostare l'applicazione come client attivo di input , che rende anche il carattere in primo piano.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





