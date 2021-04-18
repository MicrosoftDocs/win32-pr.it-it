---
title: Differenze tra i modelli a oggetti
description: Differenze tra i modelli a oggetti
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, differenze di versione
- modello a oggetti, differenze di versione
- Controllo ActiveX di Windows Media Player, differenze di versione
- Controllo ActiveX, differenze di versione
- Controllo ActiveX Windows Media Player Mobile, differenze di versione
- Windows Media Player Mobile, modello a oggetti
- Guida alla migrazione, differenze di versione
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298569"
---
# <a name="differences-between-the-object-models"></a>Differenze tra i modelli a oggetti

Esistono due differenze principali tra il modello a oggetti di Windows Media Player 6,4 e il modello a oggetti di Windows Media Player 7 o versione successiva.

-   **CLSID** Il modello a oggetti di Windows Media Player 7 o versione successiva è una partenza completa del modello a oggetti della versione 6,4. Per la specifica Component Object Model (COM) è necessario che tutte le interfacce esistenti continuino a funzionare nelle nuove versioni di un componente COM. Ciò significa che è possibile aggiungere nuove interfacce a un componente COM, ma le interfacce esistenti non devono mai essere modificate, garantendo che il codice client precedente funzioni sempre con il componente specifico che è stato progettato per l'utilizzo. Pertanto, il controllo ActiveX Windows Media Player 7 o versione successiva ha un nuovo ID classe: 6BF52A52-394A-11D3-B153-00C04F79FAA6. Se si desidera sfruttare le nuove funzionalità del controllo per questa versione, è necessario modificare il CLSID.
-   **Modello a oggetti gerarchico** Se si usa il controllo ActiveX di Windows Media Player 6,4, si è notato che è possibile accedere a tutte le proprietà, i metodi e gli eventi tramite lo stesso oggetto, ovvero l'oggetto **Player** . Al contrario, il modello a oggetti di Windows Media Player 7 o versione successiva è organizzato come una gerarchia di oggetti. L'oggetto **Player** è ancora l'oggetto radice, ma a questo punto è possibile accedere alle funzioni tramite una varietà di oggetti figlio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> </dl>

 

 




