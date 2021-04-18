---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298497"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

**IAgentCommandWindow** definisce un'interfaccia che consente alle applicazioni di impostare ed eseguire query sulle proprietà della finestra dei comandi vocali. La finestra comandi vocali è una risorsa condivisa progettata principalmente per consentire agli utenti di visualizzare i comandi abilitati per la voce. Se il riconoscimento vocale è disabilitato, la finestra dei comandi vocali viene ancora visualizzata, con il testo "input vocale disabilitato" (nella lingua del carattere). Se non è installato alcun motore vocale che corrisponda all'impostazione della lingua del carattere, viene visualizzata la finestra "input vocale non disponibile". Se il client di input-attivo non ha definito parametri vocali per i comandi e ha disabilitato i comandi vocali globali, nella finestra viene visualizzato "nessun comando vocale". È anche possibile eseguire una query sulle proprietà della finestra dei comandi vocali indipendentemente dal fatto che l'input vocale sia disabilitato o che sia installato un motore di riconoscimento vocale compatibile.

**Metodi nell'ordine Vtable**



| Metodi IAgentCommandWindow                             | Descrizione                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SetVisible**](iagentcommandwindow--setvisible.md)   | Imposta il valore della proprietà [**Visible**](visible-property.md) della finestra dei comandi vocali.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Restituisce il valore della proprietà [**Visible**](visible-property.md) della finestra dei comandi vocali. |
| [**GetPosition**](iagentcommandwindow--getposition.md) | Restituisce la posizione della finestra dei comandi vocali.                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | Restituisce le dimensioni della finestra dei comandi vocali.                                                      |



 

 

 




