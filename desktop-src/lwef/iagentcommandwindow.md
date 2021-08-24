---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80509efbe4f9d6391b3ac6ffbdf5cb02580826fd1aa7a94f1536ba5706322606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105181"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

**IAgentCommandWindow definisce** un'interfaccia che consente alle applicazioni di impostare le proprietà della finestra Comandi vocali ed eseguire query su di loro. La finestra Comandi vocali è una risorsa condivisa progettata principalmente per consentire agli utenti di visualizzare i comandi vocali. Se il riconoscimento vocale è disabilitato, viene ancora visualizzata la finestra Comandi vocali, con il testo "Input vocale disabilitato" (nella lingua del carattere). Se non è installato alcun motore di riconoscimento vocale corrispondente all'impostazione della lingua del carattere, nella finestra viene visualizzato "Input vocale non disponibile". Se il client attivo per l'input non ha definito parametri vocali per i relativi comandi e ha disabilitato i comandi vocali globali, la finestra visualizza "Nessun comando vocale". È anche possibile eseguire una query delle proprietà della finestra Comandi vocali indipendentemente dal fatto che l'input vocale sia disabilitato o che sia installato un motore di riconoscimento vocale compatibile.

**Metodi nell'ordine Vtable**



| Metodi IAgentCommandWindow                             | Descrizione                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SetVisible**](iagentcommandwindow--setvisible.md)   | Imposta il valore della [**proprietà Visible**](visible-property.md) della finestra Comandi vocali.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Restituisce il valore della [**proprietà Visible**](visible-property.md) della finestra Comandi vocali. |
| [**Getposition**](iagentcommandwindow--getposition.md) | Restituisce la posizione della finestra Comandi vocali.                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | Restituisce le dimensioni della finestra comandi vocali.                                                      |



 

 

 




