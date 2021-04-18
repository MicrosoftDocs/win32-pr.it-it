---
title: Oggetto CommandsWindow
description: Oggetto CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299607"
---
# <a name="the-commandswindow-object"></a>Oggetto CommandsWindow

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'oggetto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) fornisce l'accesso alle proprietà della finestra dei comandi vocali. La finestra comandi vocali è una risorsa condivisa progettata principalmente per consentire agli utenti di visualizzare i comandi abilitati per la voce. Se il riconoscimento vocale è disabilitato, la finestra dei comandi vocali viene ancora visualizzata, con il testo "input vocale disabilitato" (nella lingua del carattere). Se non è installato alcun motore vocale che corrisponda all'impostazione della lingua del carattere visualizzata dalla finestra, "input vocale non disponibile". Se il client di input-attivo non ha definito parametri vocali per i comandi e ha disabilitato i comandi vocali globali, nella finestra viene visualizzato "nessun comando vocale". È anche possibile eseguire una query sulle proprietà della finestra dei comandi vocali indipendentemente dal fatto che l'input vocale sia disabilitato o che sia installato un motore di riconoscimento vocale compatibile.

-   [Proprietà di CommandsWindow](commandswindow-properties.md)

 

 