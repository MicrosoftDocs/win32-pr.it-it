---
description: Descrizione delle tecniche di sottostandard per l'esposizione di controlli personalizzati.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Tecniche sottostandard per l'esposizione di controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315549"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Tecniche sottostandard per l'esposizione di controlli personalizzati

Se un'applicazione non supporta Microsoft Active Accessibility, potrebbe non essere completamente accessibile. Le tecniche seguenti eseguono il rendering dei controlli parzialmente compatibili:

-   Restituisce una stringa descrittiva quando viene eseguita una query sul controllo utilizzando il \_ messaggio WM gettext. Ad esempio, consentire a un equivalente personalizzato di un controllo Button denominato "Print" di restituire la stringa "Print button". Identifica sia il tipo di controllo che l'etichetta. La stessa stringa è appropriata per un pulsante con un'etichetta diversa dal testo, ad esempio un grafico di una stampante. Analogamente, consentire a un controllo personalizzato che si comporta come una casella di controllo di restituire la stringa della didascalia "stampa abilitata, selezionata".
-   Supporto del \_ messaggio WM GETDLGCODE, che identifica l'input da tastiera supportato. Ad esempio, consentire a un equivalente personalizzato di un controllo di modifica di gestire WM \_ GETDLGCODE restituendo DLGC \_ HASSETSEL se gestisce i messaggi per impostare la selezione, DLGC \_ WANTARROWS se usa i tasti di direzione e DLGC \_ WANTCHARS per indicare che usa l'input di caratteri.
    > [!Note]  
    > Solo i controlli con i rispettivi handle di finestra possono rispondere ai \_ messaggi WM GetText e WM \_ GETDLGCODE.

     

Per evitare problemi di compatibilità con gli strumenti di accessibilità, è necessario seguire attentamente Active Accessibility linee guida per la progettazione di controlli personalizzati. Per ulteriori informazioni su come evitare problemi di compatibilità con gli strumenti di accessibilità, vedere la sezione relativa all' [accessibilità](../accessibility/accessibility.md) .

 

 
