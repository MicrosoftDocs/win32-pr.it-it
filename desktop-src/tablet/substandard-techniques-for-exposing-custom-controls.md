---
description: Descrizione delle tecniche non standard per l'esposizione di controlli personalizzati.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Tecniche non standard per l'esposizione di controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121856bf5303b011b785a26bc47013e0df93463d7f278d6e4586991a47d8e020
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934311"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a>Tecniche non standard per l'esposizione di controlli personalizzati

Se un'applicazione non supporta Microsoft Active Accessibility, potrebbe non essere completamente accessibile. Le tecniche seguenti eseguono il rendering dei controlli parzialmente compatibili:

-   Restituisce una stringa descrittiva quando viene eseguita una query sul controllo usando il messaggio WM \_ GETTEXT. Ad esempio, consentire a un equivalente personalizzato di un controllo pulsante con etichetta "Stampa" di restituire la stringa "Pulsante di stampa". Identifica sia il tipo di controllo che l'etichetta. La stessa stringa è appropriata per un pulsante con un'etichetta diversa dal testo, ad esempio un elemento grafico di una stampante. Analogamente, consentire a un controllo personalizzato che si comporta come una casella di controllo di restituire la stringa della didascalia "Stampa abilitata casella di controllo, selezionata".
-   Supportare il messaggio WM \_ GETDLGCODE, identificando l'input da tastiera supportato. Ad esempio, consentire a un equivalente personalizzato di un controllo di modifica di gestire WM GETDLGCODE restituisce DLGC HASSETSEL se gestisce i messaggi per impostare la \_ selezione, DLGC WANTARROWS se usa i tasti di direzione e \_ \_ DLGC WANTCHARS per indicare che usa \_ l'input di caratteri.
    > [!Note]  
    > Solo i controlli con handle di finestra personalizzati possono rispondere ai messaggi WM \_ GETTEXT e WM \_ GETDLGCODE.

     

Per evitare problemi di compatibilità con gli strumenti di accessibilità, è necessario seguire Active Accessibility da vicino durante la progettazione di controlli personalizzati. Per altre informazioni su come evitare problemi di compatibilità con gli strumenti di accessibilità, vedere la [sezione Accessibilità.](../accessibility/accessibility.md)

 

 
