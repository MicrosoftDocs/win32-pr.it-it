---
title: Differenze tra i modelli a oggetti
description: Differenze tra i modelli a oggetti
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, modello a oggetti
- Windows Media Player a oggetti, differenze di versione
- modello a oggetti,differenze di versione
- Windows Media Player ActiveX controllo, differenze di versione
- ActiveX controllo, differenze di versione
- Windows Media Player Controllo delle ActiveX per dispositivi mobili, differenze di versione
- Windows Media Player Dispositivi mobili, modello a oggetti
- guida alla migrazione, differenze tra le versioni
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dd3b7862e2d9c5580950ad2eb718bd1c8125a5d22ec6a08533c140de545086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749742"
---
# <a name="differences-between-the-object-models"></a>Differenze tra i modelli a oggetti

Esistono due differenze principali tra il modello Windows Media Player 6.4 e il modello a oggetti Windows Media Player 7 o versione successiva.

-   **CLSID** Il Windows Media Player a oggetti 7 o versione successiva è una partenza completa dal modello a oggetti della versione 6.4. La Component Object Model (COM) richiede che tutte le interfacce esistenti continuino a funzionare nelle nuove versioni di un componente COM. Ciò significa che è possibile aggiungere nuove interfacce a un componente COM, ma le interfacce esistenti non devono mai essere modificate, assicurando che il codice client precedente funzioni sempre con il componente specifico per cui è stato progettato. Pertanto, il controllo ActiveX Windows Media Player 7 o versione successiva ha un nuovo ID di classe: 6BF52A52-394A-11D3-B153-00C04F79FAA6. Se si desidera sfruttare le nuove funzionalità del controllo per questa versione, è necessario modificare il CLSID.
-   **Modello a oggetti gerarchico** Se hai già utilizzato il controllo Windows Media Player 6.4 ActiveX, potresti aver notato che l'accesso a tutte le proprietà, ai metodi e agli eventi avviene tramite lo stesso oggetto: l'oggetto **Player.** Al contrario, il modello Windows Media Player 7 o versione successiva è organizzato come gerarchia di oggetti. **L'oggetto Player** è ancora l'oggetto radice, ma è ora possibile accedere alle funzioni tramite un'ampia gamma di oggetti figlio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> </dl>

 

 




