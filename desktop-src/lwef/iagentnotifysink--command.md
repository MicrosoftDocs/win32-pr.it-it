---
title: Comando IAgentNotifySink
description: Comando IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963019"
---
# <a name="iagentnotifysinkcommand"></a>Comando IAgentNotifySink::

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*
</dt> <dd>

Indirizzo dell'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per l'oggetto [**IAgentUserInput**](iagentuserinput.md) .

</dd> </dl>

Utilizzare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per recuperare l'interfaccia [**IAgentUserInput**](iagentuserinput.md) .

Il server invia una notifica al client di input attivo quando l'utente sceglie un comando mediante voce o selezionando un comando dal menu a comparsa del carattere. L'evento si verifica anche quando l'utente seleziona uno dei comandi del server. In questo caso il server restituisce un ID di comando null, il Punteggio di confidenza e il testo vocale restituiti dal motore di sintesi vocale per tale voce.

## <a name="see-also"></a>Vedere anche

[**IAgentUserInput**](iagentuserinput.md)


 

 