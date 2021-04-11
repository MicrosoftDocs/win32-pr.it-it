---
title: Valori DPI alti
description: .
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adad7c986c7083ab2327f0c8de0bd2cace5ef20a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047148"
---
# <a name="high-dpi"></a>Valori DPI alti

Poiché le tecnologie di visualizzazione avanzano, i produttori hanno aumentato il numero di pixel supportati dalle visualizzazioni. Sebbene il testo, le immagini e gli elementi dell'interfaccia utente risultino molto più nitidi e più leggibili negli schermi ad alta risoluzione, il sistema operativo deve essere scalato per supportare l'esperienza visiva; in caso contrario, tutto sembra più piccolo.

Windows 7 supporta schermi con valori *dpi* alti. I dati di mercato indicano che le distribuzioni di schermi *dpi* alti (120-144 punti per pollice (dpi)) aumenteranno nell'intervallo di tempo di Windows 7. Quando si eseguono risoluzioni native su queste schermate, molte applicazioni appaiono molto piccole a meno che non utilizzino valori *DPI alti*. Alcune applicazioni, ad esempio Windows Internet Explorer, includono funzionalità di scalabilità dei tipi di carattere che consentono agli utenti di eseguire lo zoom avanti e indietro, ma molte applicazioni non lo eseguono. Funzionalità *DPI elevata* di Windows 7:

-   Garantisce che le esperienze di Windows e delle applicazioni siano ottimali nell'hardware standard (le impostazioni *dpi* sono ottimizzate in base alle funzionalità dell'hardware).
-   Consente alla shell di Windows e ad altre applicazioni basate su Windows di avere un aspetto positivo con impostazioni *dpi* diverse.
-   Rispetta le impostazioni *dpi* predefinite basate sulle specifiche hardware e sulle funzionalità.
-   Consente agli utenti di personalizzare le impostazioni *dpi* senza riavvio.
-   Garantisce che la schermata sia sempre impostata sulla risoluzione nativa.

La funzionalità di scalabilità *dpi* Windows consente di ridimensionare i tipi di carattere e gli elementi dell'interfaccia utente, ad esempio pulsanti, icone e campi di input, in base a una percentuale calcolata, come specificato dall'impostazione *dpi* . Si tratta di una differenza rispetto al ridimensionamento che si verifica quando la risoluzione dello schermo è ridotta. Nel caso di scalabilità *dpi* , Windows fornisce i tipi di carattere e gli elementi dell'interfaccia utente disegnati con più pixel, ottenendo un'esperienza di Windows più ampia, di maggiore fedeltà e più nitida. Le applicazioni Windows di terze parti possono sfruttare le impostazioni *DPI elevate* e modificare di conseguenza l'interfaccia utente, dichiarando la compatibilità con *DPI elevata* . Gli sviluppatori di applicazioni non dovrebbero più presumere che 96 dpi sia la soluzione ideale per tutte le applicazioni.

Per ulteriori informazioni su *DPI alti* e sulla scrittura di applicazioni con compatibilità *dpi* elevata, vedere valori [dpi](../hidpi/high-dpi-desktop-application-development-on-windows.md)alti.

 

 