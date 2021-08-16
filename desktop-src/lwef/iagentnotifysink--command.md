---
title: Comando IAgentNotifySink
description: Comando IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d9c20de96c1bb14cf003ad7beff98e716e272ad3de39532d9b455e279d97af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105204"
---
# <a name="iagentnotifysinkcommand"></a>IAgentNotifySink::Command

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Notifica a un'applicazione client che un [**comando**](/windows/desktop/lwef/the-command-object) è stato selezionato dall'utente.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificatore dell'alternativa del comando di corrispondenza migliore.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*inputUserInput*
</dt> <dd>

Indirizzo [**dell'interfaccia IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per [**l'oggetto IAgentUserInput.**](iagentuserinput.md)

</dd> </dl>

Usare [**QueryInterface per**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) recuperare [**l'interfaccia IAgentUserInput.**](iagentuserinput.md)

Il server invia una notifica al client attivo di input quando l'utente sceglie un comando per voce o selezionando un comando dal menu a comparsa del carattere. L'evento si verifica anche quando l'utente seleziona uno dei comandi del server. In questo caso il server restituisce un ID di comando Null, il punteggio di attendibilità e il testo vocale restituito dal motore di riconoscimento vocale per tale voce.

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput**](iagentuserinput.md)


 

 